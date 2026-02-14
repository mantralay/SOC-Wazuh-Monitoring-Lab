# 4. Ban Validation

## Objective
To confirm that Fail2Ban successfully detected repeated SSH failures and automatically banned the attacker IP.

## Verification Command

The following command was used to verify ban status:

# Command - sudo fail2ban-client status sshd

# Output

Link -

Status for the jail: sshd
Currently failed: 1
Total failed: 13
Currently banned: 1
Total banned: 2
Banned IP list: 192.168.71.xxx


## Analysis

- Total failed attempts increased due to repeated authentication failures.
- After exceeding the configured threshold (maxretry = 5), the attacker IP was banned.
- The banned IP matched the Kali Linux machine.
- SSH connections from the attacker were immediately blocked.

## SSH Access Validation

After ban enforcement, attempts to reconnect from Kali using:

# Command in Kali Linux - ssh root@192.168.71.130


Resulted in:
- Connection refused
- Timeout
- Immediate denial

This confirms firewall-level blocking was active.

## Security Impact

This demonstrates automated containment of brute-force attacks without manual intervention.

Fail2Ban successfully:
- Detected malicious behavior
- Enforced temporary firewall ban
- Prevented further attack attempts
