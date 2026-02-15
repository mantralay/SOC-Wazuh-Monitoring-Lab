# 1. Environment Overview

## Objective

To design, implement, and validate a custom Wazuh detection rule for identifying suspicious sudo activity.

This project focuses on detection engineering and custom rule development within Wazuh SIEM.

---

## Lab Architecture

Target System:
- Ubuntu Server 24.04
- Wazuh Manager (All-in-one deployment)

Monitoring:
- Wazuh SIEM
- Local log monitoring (/var/log/auth.log)

Virtualization:
- VMware
- NAT networking

---

## Security Scenario

An attacker attempts privilege escalation by repeatedly entering incorrect sudo passwords.

The objective is to:

- Analyze the raw authentication logs
- Identify the log pattern
- Create a custom Wazuh rule
- Assign severity level
- Validate alert triggering

---

## Why Custom Rules Matter

Default SIEM rules may not detect all organization-specific threats.

Custom rules allow:

- Tailored detection logic
- Environment-specific monitoring
- Enhanced alert accuracy
- Threat hunting customization

This is an essential SOC and Blue Team engineering skill.
