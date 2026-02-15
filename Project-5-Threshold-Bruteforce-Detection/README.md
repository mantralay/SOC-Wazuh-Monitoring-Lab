# 🔹 Project 5 – Threshold-Based SSH Brute Force Detection

## 🎯 Objective

Detect SSH brute-force attacks using a custom threshold-based rule in Wazuh SIEM.

This project enhances basic detection by identifying multiple failed login attempts within a defined timeframe.

---

## 🛠 Lab Environment

- Ubuntu Server 24.04
- Wazuh SIEM (All-in-one deployment)
- Kali Linux (Attack simulation)
- Hydra
- VMware Workstation

---

## 🧠 Detection Logic

This project uses rule chaining and threshold correlation:

1. Base Rule 5710 → SSH login failure
2. Custom Rule 100100 → Single SSH failed login alert
3. Threshold Rule 100200 → 3 failed attempts within 60 seconds

---

## 🧩 Custom Rule Configuration

```xml
<group name="ssh_bruteforce,custom,">

  <!-- Single failed SSH login detection -->
  <rule id="100100" level="10">
    <if_sid>5710</if_sid>
    <description>Custom Alert: SSH failed login detected</description>
    <mitre>
      <id>T1110</id>
    </mitre>
  </rule>

  <!-- Threshold-based brute force detection -->
  <rule id="100200" level="12" frequency="3" timeframe="60">
    <if_matched_sid>100100</if_matched_sid>
    <description>High Alert: SSH brute-force attack detected (3 failures in 60 seconds)</description>
    <mitre>
      <id>T1110</id>
    </mitre>
  </rule>

</group>

---

## 🚨 Attack Simulation

Hydra Command Used:
hydra -l fakeuser -P small_wordlist.txt -t 1 ssh://TARGET_IP

---

## 📊 Detection Results

1. Rule 100100 triggered on each failed login

2. Rule 100200 triggered when threshold exceeded

3. Alert Level: 12 (High Severity)

4. MITRE ATT&CK Mapping: T1110 – Brute Force

---

## 🧠 SOC Investigation Focus

1. Alert frequency analysis

2. Timestamp correlation

3. Source IP identification

4. Threshold validation

5. Attack pattern recognition

---

## 🧠 SOC Investigation Focus

1.Alert frequency analysis

2. Timestamp correlation

3. Source IP identification

4. Threshold validation

5. Attack pattern recognition
