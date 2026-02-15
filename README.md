# SOC Analyst Portfolio – Wazuh SIEM Lab

This repository contains hands-on Security Operations Center (SOC) lab projects demonstrating detection, prevention, and investigation of real-world attack scenarios using Wazuh SIEM.

All projects were built in a controlled virtual lab environment using Ubuntu Server and VMware.

---

## 🔹 Project 1 – SSH Brute-Force Detection

**Objective:** Detect SSH brute-force attacks using Wazuh SIEM.

➡ **View Project:**  
[Open Project 1](Project-1-SSH-Bruteforce-Detection)

**Key Highlights:**
- Simulated SSH brute-force attack using Hydra
- Generated 1000+ failed authentication attempts
- Analyzed authentication failure spikes
- Investigated alert severity and timestamps
- Mapped detection to MITRE ATT&CK (T1110 – Brute Force)

**Core Skills:**
- SIEM Monitoring
- Log Analysis
- Threat Detection
- SOC Alert Investigation

---

## 🔹 Project 2 – SSH Intrusion Prevention (Fail2Ban)

**Objective:** Implement automated response to block brute-force attackers.

➡ **View Project:**  
[Open Project 2](Project-2-SSH-Intrusion-Prevention)

**Key Highlights:**
- Installed and configured Fail2Ban
- Configured SSH jail rules
- Triggered controlled brute-force attack
- Verified automatic IP banning
- Validated prevention logs in Wazuh

**Core Skills:**
- Intrusion Prevention
- Linux Security Hardening
- Automated Incident Response
- Log Validation & Monitoring

---

## 🔹 Project 3 – File Integrity Monitoring (FIM)

**Objective:** Detect unauthorized modification of critical system files using Wazuh FIM.

➡ **View Project:**  
[Open Project 3](Project-3-File-Integrity-Monitoring)

**Key Highlights:**
- Enabled real-time File Integrity Monitoring
- Simulated attacker tampering of `/etc/hosts`
- Detected checksum change (Rule 550 – Level 7)
- Investigated hash differences and timestamps
- Performed structured SOC alert analysis

**Core Skills:**
- File Integrity Monitoring
- Hash Comparison Analysis
- Real-Time Security Monitoring
- Incident Validation
- MITRE ATT&CK Mapping

---

## 🛠 Lab Environment

- Ubuntu Server 24.04
- Wazuh SIEM (All-in-one deployment)
- VMware Workstation
- Kali Linux (Attack simulation)
- Hydra
- Fail2Ban

---

## 🎯 Portfolio Skills Demonstrated

- SIEM Deployment & Configuration
- Log Monitoring & Alert Triage
- Brute-force Detection
- Intrusion Prevention
- File Integrity Monitoring
- MITRE ATT&CK Mapping
- Linux Administration
- SOC-Level Investigation & Documentation

---

This portfolio demonstrates practical hands-on experience aligned with entry-level SOC Analyst and Blue Team roles.
