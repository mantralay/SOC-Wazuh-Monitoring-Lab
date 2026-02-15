# 🧠 Investigation – SSH Brute Force Detection

## Scenario

Hydra was used from Kali Linux to simulate an SSH brute-force attack against the Ubuntu server.

---

## Detection Timeline

- Multiple rule 100100 alerts observed.
- Threshold rule 100200 triggered after 5 failures within 60 seconds.

---

## Alert Evidence

- Source IP: Kali Linux machine
- Target Service: SSH (Port 22)
- Technique: Password Guessing
- MITRE ATT&CK: T1110

---

## SOC Analysis

This attack demonstrates:

- Credential access attempts
- Automated brute-force behavior
- Rapid authentication failures within short timeframe

---

## Conclusion

The custom threshold rule successfully escalated repeated failed login attempts into a high-severity alert, simulating real-world SOC detection logic.
