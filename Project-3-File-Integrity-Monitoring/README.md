# Project 3 – File Integrity Monitoring (FIM) Detection Lab

## Project Overview

This project demonstrates how Wazuh File Integrity Monitoring (FIM) detects unauthorized file modifications on a Linux system in real-time.

The lab simulates an attacker modifying a critical system configuration file and investigates the generated security alert from a SOC analyst perspective.

---

## Objective

To validate Wazuh’s ability to:

- Detect file modifications
- Identify checksum changes
- Generate real-time alerts
- Support SOC-level alert investigation

---

## Lab Environment

- Ubuntu Server 24.04
- Wazuh Manager (All-in-one deployment)
- VMware Workstation
- NAT Networking

---

## Attack Simulation

The `/etc/hosts` file was modified using:

Command - echo "8.8.8.8 new-test-entry" | sudo tee -a /etc/hosts


This simulates unauthorized configuration tampering.

---

## Detection Mechanism

Wazuh File Integrity Monitoring (FIM):

- Monitored `/etc` directory in real-time
- Detected hash mismatch
- Triggered Rule ID 550
- Generated Level 7 alert

Alert Description:
> Integrity checksum changed

---

## SOC Investigation

The alert analysis confirmed:

- File path affected: `/etc/hosts`
- Hash value changed
- Timestamp matched modification time
- Monitoring agent successfully reported event

This demonstrates practical SOC workflow:

- Alert validation
- Integrity verification
- Threat classification
- Incident documentation

---

## Skills Demonstrated

- SIEM configuration
- File Integrity Monitoring setup
- Real-time security monitoring
- Alert triage and investigation
- Linux system administration
- MITRE ATT&CK mapping
- Incident analysis documentation

---

## Conclusion

This project validates that Wazuh can detect unauthorized file modifications in real-time and supports SOC-level incident investigation.

File Integrity Monitoring is critical for detecting:

- Persistence mechanisms
- Configuration tampering
- Malware modification
- Insider threats
- Compliance violations
