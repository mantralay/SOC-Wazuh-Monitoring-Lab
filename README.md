# SOC Wazuh Monitoring Lab

This repository contains hands-on SOC Analyst projects built in a controlled virtual lab environment using Wazuh SIEM.

The objective of this lab is to simulate real-world attack scenarios and perform detection, investigation, and prevention using industry-standard tools.

---

## Lab Environment

- Ubuntu Server 24.04
- Wazuh SIEM (All-in-one deployment)
- Kali Linux (Attacker)
- VMware Virtualization
- SSH Service
- Hydra (Attack Simulation)
- Fail2Ban (Intrusion Prevention)

---

## Projects Included

### 🔍 Project 1 – SSH Brute-Force Detection
Focus: Detection & Investigation

- Simulated SSH brute-force attack
- Generated 1000+ failed authentication attempts
- Analyzed authentication failure spikes
- Mapped alerts to MITRE ATT&CK (T1110)
- Performed SOC-style log investigation

➡ View Project:  
`Project-1-SSH-Bruteforce-Detection/`

---

### 🔐 Project 2 – SSH Intrusion Prevention
Focus: Automated Containment & Validation

- Configured Fail2Ban for SSH protection
- Automatically banned attacker IP
- Enforced firewall-level blocking
- Validated containment using Wazuh SIEM
- Demonstrated layered security approach

➡ View Project:  
`Project-2-SSH-Intrusion-Prevention/`

---

## Skills Demonstrated

- SIEM Deployment & Monitoring
- Log Analysis & Alert Investigation
- SSH Security Hardening
- Intrusion Detection & Prevention
- MITRE ATT&CK Mapping
- Linux System Administration
- Incident Response Validation

---

## Objective

To build practical SOC Analyst skills through hands-on attack simulation, detection, investigation, and automated prevention.

This lab demonstrates the complete attack lifecycle:

Detection → Analysis → Containment → Validation


