# 3. Attack Simulation

## Objective
To simulate an SSH brute-force attack against the Ubuntu server in order to test Fail2Ban's automatic blocking capability.

## Attack Tool
Hydra (Kali Linux)

## Target
Ubuntu Server (SSH service on port 22)

## Controlled Attack Command

A controlled attack was used instead of a full wordlist to avoid unnecessary log flooding:

# Command - hydra -t 4 -l root -p wrongpassword ssh://192.168.71.130


## Command Explanation

- -t 4  
  Uses 4 parallel threads.

- -l root  
  Attempts login as root user.

- -p wrongpassword  
  Forces authentication failure to trigger Fail2Ban.

- ssh://192.168.71.130  
  Target Ubuntu server IP.

## Expected Behavior

- Multiple failed SSH login attempts generated.
- Fail2Ban detects repeated failures.
- After 5 failed attempts (maxretry), attacker IP is banned.
- SSH connections from attacker are blocked.

## Observed Behavior

- Hydra initially attempted authentication.
- After threshold exceeded, SSH connections were refused.
- Fail2Ban automatically added firewall rule blocking attacker IP.
