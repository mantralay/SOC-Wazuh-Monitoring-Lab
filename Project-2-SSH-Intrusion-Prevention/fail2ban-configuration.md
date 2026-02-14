# 2. Fail2Ban Configuration

## Objective
To configure Fail2Ban to automatically block SSH brute-force attempts after repeated authentication failures.

## Installation

Fail2Ban was installed on the Ubuntu server using:

sudo apt update
sudo apt install fail2ban -y

Service status was verified:

sudo systemctl status was verified:
## SSH Jail Configuration

The default configuration file was copied to create a local configuration:

sudo cp /etc/fail2ban/jail.conf/etc/fail2ban/jail.local

The `[sshd]` jail section was modified as follows:

[sshd]
enabled = true
port = ssh
logpath = %(sshd_log)s
backend = systemd
maxretry = 5
findtime = 600
bantime = 600


## Configuration Explanation

- enabled = true  
  Activates SSH protection.

- maxretry = 5  
  Bans an IP after 5 failed login attempts.

- findtime = 600  
  The 5 failures must occur within 10 minutes.

- bantime = 600  
  The IP is banned for 10 minutes.

- backend = systemd  
  Required for Ubuntu 24.04 log handling.

## Jail Verification

After restarting Fail2Ban:

sudo systemctl restart fail2ban

The active jail was verified:

sudo fail2ban-client status
sudo fail2ban-client status sshd


This confirmed that the SSH jail was active and monitoring login attempts.

