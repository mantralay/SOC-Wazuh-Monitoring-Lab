# Project 1 – SSH Brute-Force Detection Using Wazuh SIEM

---

## Overview

This project demonstrates detection and investigation of an SSH brute-force attack using Wazuh SIEM in a controlled lab environment.

The focus of this project is:

- Log-based attack detection
- Authentication failure analysis
- MITRE ATT&CK mapping
- SOC-style alert investigation

---

## Lab Environment

**Attacker Machine**
- Kali Linux
- Hydra (Brute-force tool)

**Target Machine**
- Ubuntu Server 24.04
- Wazuh SIEM (All-in-one deployment)

**Network Setup**
- VMware virtual lab
- NAT configuration
- SSH enabled on target

---

## Attack Simulation

Hydra was used to simulate an SSH brute-force attack:

Hydra Command - hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://192.168.71.130


### Result:
- 1000+ failed authentication attempts generated
- Continuous login failures recorded in system logs
- High-volume alert spike observed in Wazuh dashboard

---

## Detection in Wazuh

Wazuh successfully detected:

- Multiple authentication failures
- SSH login attempts from a single source IP
- Alert severity classification
- Event timestamps and source IP tracking

### MITRE ATT&CK Mapping

Detected activity mapped to:

- T1110 – Brute Force
- T1110.001 – Password Guessing

---

## SOC Investigation Process

The following investigation steps were performed:

1. Identified spike in authentication failures
2. Analyzed source IP address
3. Reviewed timestamps and frequency
4. Checked for successful login attempts
5. Confirmed no system compromise

---

## Key Findings

- Attack pattern matched automated brute-force behavior
- No successful authentication occurred
- Logs were correctly ingested and correlated
- SIEM detection worked as expected

---

## Skills Demonstrated

- SIEM Deployment & Configuration
- SSH Log Analysis
- Brute-force Attack Detection
- MITRE ATT&CK Mapping
- Alert Investigation
- SOC Incident Analysis

---

## Evidence

Screenshots included in the `screenshots/` directory show:

- Authentication failure spike
- MITRE ATT&CK mapping
- Alert dashboard
- Event timeline analysis
