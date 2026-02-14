# 1. Environment Setup

## Objective
To implement automated SSH brute-force prevention using Fail2Ban and validate containment using Wazuh SIEM.

## Lab Architecture

Attacker Machine:
- Kali Linux

Target Machine:
- Ubuntu Server 24.04
- Wazuh SIEM (All-in-one deployment)
- Fail2Ban (Host-based Intrusion Prevention)

## Network Configuration
- Virtualized environment (VMware)
- NAT networking
- Kali → Ubuntu SSH communication enabled

## Tools Used
- Hydra (attack simulation)
- Fail2Ban (intrusion prevention)
- Wazuh (SIEM monitoring)
- OpenSSH

## Initial Security State
- SSH service running
- Root login enabled for testing
- Wazuh actively monitoring authentication logs
