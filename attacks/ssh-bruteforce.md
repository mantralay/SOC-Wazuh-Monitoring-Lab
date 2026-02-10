# SSH Brute-Force Attack Simulation

## Objective
To simulate an SSH brute-force attack and observe detection in Wazuh SIEM.

## Environment
- Attacker: Kali Linux
- Target: Ubuntu Server
- Service: SSH (Port 22)

## Tool Used
Hydra

## Command Executed
hydra -t 4 -l root -P /usr/share/wordlists/rockyou.txt ssh://192.168.71.130

## Attack Description
Hydra was used to perform repeated SSH login attempts using a password wordlist, generating high-volume authentication failures.

## Result
- 1000+ failed SSH authentication attempts
- No successful login
- Automated brute-force behavior identified

## SOC Relevance
SSH brute-force attacks are common initial-access techniques used by attackers to compromise systems.
