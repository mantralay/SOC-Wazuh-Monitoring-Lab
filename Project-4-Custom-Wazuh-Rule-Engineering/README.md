# Project 4 – Custom Wazuh Rule Engineering

## 🎯 Objective

Design and implement a custom Wazuh detection rule to identify failed sudo authentication attempts and elevate alert severity using rule correlation.

---

## 🛠 Lab Environment

- Ubuntu Server 24.04
- Wazuh SIEM (All-in-One)
- VMware Workstation
- Kali Linux (attack simulation)

---

## 🔎 Detection Scenario

Default Wazuh rule:
- Rule ID: 5503
- Description: PAM: User login failed.
- Level: 5

Custom Rule Created:
- Rule ID: 100100
- Level: 10
- Correlated using `<if_sid>5503</if_sid>`
- Mapped to MITRE ATT&CK T1068

---

## 🧠 Rule Logic

The custom rule triggers when Wazuh detects a failed sudo login event (rule 5503).  
It increases severity to level 10 to simulate high-priority SOC alerting.

---

## 📊 Validation Steps

1. Created custom rule in `/var/ossec/etc/rules/local_rules.xml`
2. Validated configuration:

commnad - sudo /var/ossec/bin/wazuh-analysisd -t

3. Restarted manager:

command - sudo systemctl restart wazuh-manager

4. Generated failed sudo login attempt
5. Verified alert in Wazuh dashboard using:

rule.id:100100


---

## 📈 Detection Result

- Alert successfully triggered
- Severity increased to Level 10
- MITRE ATT&CK mapping confirmed
- Custom rule parsed correctly

---

## 🏆 Skills Demonstrated

- Wazuh Rule Development
- SIEM Alert Engineering
- Rule Correlation
- MITRE ATT&CK Mapping
- SOC-Level Alert Investigation
- Detection Engineering
