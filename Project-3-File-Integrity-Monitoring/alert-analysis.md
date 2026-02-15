# 4. Alert Analysis

## Alert Summary

- Rule ID: 550
- Rule Description: Integrity checksum changed
- Alert Level: 7 (Medium Severity)
- Monitored File: /etc/hosts
- Detection Module: Wazuh File Integrity Monitoring (FIM)

---

## What Happened

A modification was made to the `/etc/hosts` file on the Ubuntu server.

Wazuh detected that the file’s checksum (hash value) changed compared to its previously stored baseline.

This triggered a Level 7 alert indicating file integrity violation.

---

## Technical Details Observed

When expanding the alert in Wazuh:

- data.path shows: `/etc/hosts`
- data.hash_before contains original checksum
- data.hash_after contains modified checksum
- Timestamp confirms exact time of change
- Agent name confirms the affected host

The hash mismatch confirms the file contents were altered.

---

## Root Cause

The modification was intentionally performed for lab simulation:

Command - echo "8.8.8.8 new-test-entry" | sudo tee -a /etc/hosts


This simulates an attacker altering system configuration.

---

## Why This Matters

Unauthorized modification of critical system files can indicate:

- Persistence mechanism
- DNS redirection attacks
- Malware tampering
- Privilege escalation attempts
- Insider threat activity

Monitoring such changes is critical for SOC operations.

---

## MITRE ATT&CK Mapping

Potential technique mappings:

- T1565 – Data Manipulation
- T1070 – Indicator Removal (in advanced scenarios)
- Persistence-related techniques

---

## SOC Analyst Response Process

1. Validate affected file path
2. Compare hash_before and hash_after
3. Confirm whether change was authorized
4. Check user activity around timestamp
5. Revert unauthorized modification if malicious
6. Escalate if suspicious activity is confirmed

---

## Outcome

Wazuh successfully detected the file modification in real-time.

This validates the effectiveness of File Integrity Monitoring for detecting unauthorized system changes.
