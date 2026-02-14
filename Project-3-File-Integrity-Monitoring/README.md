# 1. Environment Overview

## Objective

To detect unauthorized file modifications using Wazuh File Integrity Monitoring (FIM) and perform SOC-style alert investigation.

---

## Lab Architecture

Target System:
- Ubuntu Server 24.04
- Wazuh Manager + Agent (All-in-one deployment)

Monitoring Tool:
- Wazuh SIEM
- File Integrity Monitoring (FIM) module

Virtualization:
- VMware
- NAT networking

---

## Security Context

File Integrity Monitoring (FIM) is used to:

- Detect unauthorized file modifications
- Identify suspicious configuration changes
- Monitor sensitive directories
- Detect potential malware persistence
- Support compliance monitoring

---

## Threat Scenario

An attacker modifies a critical system file on the Ubuntu server.

Wazuh FIM detects:

- File modification
- Timestamp change
- Permission change (if applicable)
- Hash difference (before vs after)

SOC analyst investigates the alert to determine:

- What changed
- When it changed
- Who modified it
- Whether it is malicious
