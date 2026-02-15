# SOC Analyst Projects – Wazuh SIEM Lab

This repository contains hands-on SOC Analyst lab projects demonstrating detection, prevention, and investigation of security threats using Wazuh SIEM.

All projects were built in a controlled virtual lab environment using Ubuntu Server and VMware.

---

# 🔹 Project 1 – SSH Brute-Force Detection

**Objective:**  
Detect SSH brute-force attacks using Wazuh SIEM.

➡ **View Project:**  
[Open Project 1](Project-1-SSH-Bruteforce-Detection)

**Key Activities:**
- Simulated SSH brute-force attack using Hydra
- Generated 1000+ failed authentication attempts
- Observed authentication failure spikes
- Analyzed alert severity and timestamps
- Mapped detection to MITRE ATT&CK (T1110 – Brute Force)

**Skills Demonstrated:**
- SIEM monitoring
- Log analysis
- Attack simulation
- SOC alert investigation

---

# 🔹 Project 2 – SSH Intrusion Prevention (Fail2Ban)

**Objective:**  
Implement automated response to block brute-force attackers.

➡ **View Project:**  
[Open Project 2](Project-2-SSH-Intrusion-Prevention)

**Key Activities:**
- Installed and configured Fail2Ban
- Configured SSH jail rules
- Triggered brute-force attack
- Verified automatic IP banning
- Observed prevention logs in Wazuh

**Skills Demonstrated:**
- Intrusion prevention
- Linux security hardening
- Automated incident response
- Log validation and monitoring

---

# 🔹 Project 3 – File Integrity Monitoring (FIM)

**Objective:**  
Detect unauthorized modification of critical system files using Wazuh FIM.

➡ **View Project:**  
[Open Project 3](Project-3-File-Integrity-Monitoring)

**Key Activities:**
- Enabled real-time File Integrity Monitoring
- Modified `/etc/hosts` to simulate attacker tampering
- Detected checksum change (Rule 550)
- Investigated hash differences and timestamps
- Performed SOC-style alert analysis

**Detection Details:**
- Rule ID: 550
- Alert Level: 7
- Description: Integrity checksum changed

**Skills Demonstrated:**
- File Integrity Monitoring configuration
- Real-time alert detection
- Hash comparison analysis
- Incident validation
- MITRE ATT&CK mapping

---

# 🛠 Lab Environment

- Ubuntu Server 24.04
- Wazuh SIEM (All-in-one deployment)
- VMware Workstation
- Kali Linux (Attack simulation)
- Hydra
- Fail2Ban

---

# 📚 Skills Gained From This Portfolio

- SIEM Deployment & Configuration
- Log Monitoring & Alert Triage
- Brute-force Detection
- Intrusion Prevention
- File Integrity Monitoring
- MITRE ATT&CK Mapping
- Linux Administration
- SOC-Level Investigation & Documentation
