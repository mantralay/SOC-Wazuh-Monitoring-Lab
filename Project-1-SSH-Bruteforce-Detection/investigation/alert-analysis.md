# SOC Alert Investigation Report

## Incident Summary
A large number of SSH authentication failures were detected by Wazuh SIEM, indicating a brute-force attack.

## Timeline
- Detection Window: Last 10 minutes
- Total Events: 1000+ authentication failures

## Indicators of Compromise (IOCs)
- Source IP: Kali Linux attacker machine
- Destination IP: Ubuntu Server
- Target Service: SSH (Port 22)

## Detection Details
- Log Source: /var/log/auth.log
- Alert Type: Authentication failure
- Detection Method: Threshold-based correlation

## MITRE ATT&CK Mapping
- T1110 – Brute Force
- T1110.001 – Password Guessing

## Analysis
Repeated failed login attempts in a short time window indicate automated brute-force activity. No successful authentication occurred.

## Recommended Mitigation
- Disable root login over SSH
- Enable SSH key-based authentication
- Implement Fail2Ban
- Apply rate limiting

## Conclusion
This incident confirms effective detection of brute-force attacks using Wazuh SIEM and validates SOC monitoring capability.