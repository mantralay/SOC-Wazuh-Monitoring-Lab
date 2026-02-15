# 🔎 Rule Validation

## Rule 100100 – Single Failed SSH Login

**Base Rule:** 5710  
**Description:** Custom alert triggered for every failed SSH login attempt.  
**Alert Level:** 8  

Verified in Wazuh Dashboard using:
rule.id:100100

---

## Rule 100200 – Threshold Detection

**Trigger Condition:**  
5 failed SSH login attempts within 60 seconds.

**Alert Level:** 12  
**MITRE Mapping:** T1110 – Brute Force  

Verified in Wazuh Dashboard using:
rule.id:100200

---

## Validation Command Used

```bash
sudo /var/ossec/bin/wazuh-analysisd -t

Result: Configuration OK.

