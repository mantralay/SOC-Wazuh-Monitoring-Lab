# SOC Wazuh Monitoring Lab

## 📌 Project Overview
This project demonstrates a hands-on SOC Analyst lab using Wazuh SIEM to detect and investigate SSH brute-force attacks in a controlled environment.

## 🛠 Tools Used
- Wazuh SIEM
- Ubuntu Server 24.04
- Kali Linux
- Hydra
- MITRE ATT&CK Framework

## 🧪 Attack Simulation
- Simulated SSH brute-force attack using Hydra
- Generated 1000+ failed authentication attempts
- Observed real-time alerts in Wazuh dashboard

## 🔍 Detection & Analysis
- Authentication failure spikes detected
- Alerts mapped to MITRE ATT&CK:
  - T1110 – Brute Force
  - T1110.001 – Password Guessing
- Analyzed alert severity, timestamps, and source IPs

## 📊 Evidence
Screenshots of alerts and dashboards are included in the `scree
nshots/` directory.

## 🎯 Skills Demonstrated
- SIEM deployment and configuration
- Log analysis and alert investigation
- Attack simulation and detection
- SOC-style incident analysis