# SOC Analyst Projects – Wazuh SIEM Lab

This repository contains hands-on SOC Analyst lab projects demonstrating detection, prevention, monitoring, and custom detection engineering using Wazuh SIEM in a controlled virtual lab environment.

All projects were built using Ubuntu Server, VMware Workstation, and real attack simulations.

---

# 🔹 Project 1 – SSH Brute-Force Detection

**Objective:**  
Detect SSH brute-force attacks using Wazuh SIEM.

➡ **View Project:**  
[Open Project 1](Project-1-SSH-Bruteforce-Detection)

**Key Activities:**
- Simulated SSH brute-force attack using Hydra
- Generated 1000+ failed authentication attempts
- Observed authentication failure spikes in dashboard
- Analyzed alert severity, timestamps, and source IPs
- Mapped detection to MITRE ATT&CK (T1110 – Brute Force)

**Skills Demonstrated:**
- SIEM Monitoring
- Log Analysis
- Attack Simulation
- SOC Alert Investigation
- MITRE ATT&CK Mapping

---

# 🔹 Project 2 – SSH Intrusion Prevention (Fail2Ban)

**Objective:**  
Implement automated response to block brute-force attackers.

➡ **View Project:**  
[Open Project 2](Project-2-SSH-Intrusion-Prevention)

**Key Activities:**
- Installed and configured Fail2Ban
- Configured SSH jail policies
- Triggered brute-force attack
- Verified automatic IP banning
- Monitored prevention logs inside Wazuh

**Skills Demonstrated:**
- Intrusion Prevention
- Linux Security Hardening
- Automated Incident Response
- Log Validation & Monitoring
- Defensive Security Engineering

---

# 🔹 Project 3 – File Integrity Monitoring (FIM)

**Objective:**  
Detect unauthorized modification of critical system files using Wazuh File Integrity Monitoring.

➡ **View Project:**  
[Open Project 3](Project-3-File-Integrity-Monitoring)

**Key Activities:**
- Enabled real-time File Integrity Monitoring
- Modified `/etc/hosts` to simulate attacker tampering
- Detected checksum change (Rule 550)
- Investigated hash differences and timestamps
- Performed SOC-style alert validation

**Detection Details:**
- Rule ID: 550
- Alert Level: 7
- Description: Integrity checksum changed

**Skills Demonstrated:**
- File Integrity Monitoring Configuration
- Real-Time Alert Detection
- Hash Comparison Analysis
- Incident Validation
- MITRE ATT&CK Mapping

---

# 🔹 Project 4 – Custom Wazuh Rule Engineering

**Objective:**  
Design and implement a custom Wazuh detection rule using rule correlation to escalate authentication failure alerts.

➡ **View Project:**  
[Open Project 4](Project-4-Custom-Wazuh-Rule-Engineering)

**Key Activities:**
- Developed custom rule using `<if_sid>` correlation
- Elevated alert severity to Level 10
- Validated rule syntax using `wazuh-analysisd -t`
- Triggered real failed sudo login events
- Verified detection in Wazuh dashboard

**Custom Rule Details:**
- Custom Rule ID: 100100
- Parent Rule ID: 5503
- Final Severity Level: 10
- MITRE Mapping: T1068 – Privilege Escalation

**Skills Demonstrated:**
- Detection Engineering
- SIEM Rule Development
- Alert Correlation
- MITRE ATT&CK Mapping
- SOC-Level Investigation
- Log Pattern Matching

---

# 🔹 Project 5 – Threshold-Based SSH Brute Force Detection

**Objective:**  
Detect SSH brute-force attacks using custom threshold-based correlation rules.

➡ **View Project:**  
[Open Project 5](Project-5-Threshold-Bruteforce-Detection)

**Key Activities:**
- Created custom Wazuh rules
- Implemented frequency & timeframe correlation
- Simulated brute-force attack using Hydra
- Triggered high-severity alert (Level 12)
- Mapped detection to MITRE ATT&CK (T1110)

**Skills Demonstrated:**
- Advanced SIEM rule creation
- Event correlation logic
- SOC-level alert analysis
- Attack pattern detection
- Security monitoring enhancement

# 🛠 Lab Environment

- Ubuntu Server 24.04
- Wazuh SIEM (All-in-One Deployment)
- VMware Workstation
- Kali Linux (Attack Simulation)
- Hydra
- Fail2Ban

---

# 📚 Skills Demonstrated Across Portfolio

- SIEM Deployment & Configuration
- Log Monitoring & Alert Triage
- Brute-Force Detection
- Intrusion Prevention Engineering
- File Integrity Monitoring (FIM)
- Custom Rule Development
- Detection Engineering
- MITRE ATT&CK Mapping
- Linux Administration
- SOC Investigation & Documentation

---

# 🚀 Portfolio Purpose

This repository demonstrates practical SOC Analyst capabilities including detection, prevention, investigation, and alert engineering using enterprise-style SIEM workflows.

All projects are structured with:

- Setup documentation
- Attack simulation
- Alert validation
- Investigation notes
- Detection logic explanation
- MITRE ATT&CK mapping
