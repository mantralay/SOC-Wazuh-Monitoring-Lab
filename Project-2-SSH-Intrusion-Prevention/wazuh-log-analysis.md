# 5. Wazuh Log Analysis

## Objective
To analyze authentication activity and validate attack detection and containment using Wazuh SIEM.

## Pre-Ban Observation

During the brute-force simulation:

- A significant spike in SSH authentication failures was observed.
- Events were recorded under:
  - Authentication failure
  - SSH login attempts
- MITRE ATT&CK mapping included:
  - T1110 – Brute Force
  - T1110.001 – Password Guessing

This confirmed that Wazuh successfully detected malicious login behavior.

## Post-Ban Observation

After Fail2Ban triggered the ban:

- Authentication failures sharply decreased.
- SSH connections from the attacker were blocked.
- No additional successful login events were observed.

This indicates successful containment.

## Event Correlation

The following sequence was observed:

1. Multiple SSH authentication failures.
2. Threshold exceeded (5 attempts within 600 seconds).
3. Fail2Ban triggered ban.
4. Firewall rule enforced.
5. Authentication event rate reduced.

## SOC Interpretation

From a SOC perspective:

- The activity matched automated brute-force behavior.
- No evidence of successful compromise was found.
- Containment was automatically enforced.
- Risk level reduced after mitigation.

## Security Outcome

The combined use of Wazuh (detection) and Fail2Ban (prevention) demonstrates:

- Real-time threat detection
- Automated response capability
- Log-based containment validation
- Reduced attack surface exposure

This validates the effectiveness of layered security controls.
