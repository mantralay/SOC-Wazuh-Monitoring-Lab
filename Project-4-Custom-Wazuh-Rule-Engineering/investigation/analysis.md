# Investigation Analysis – Custom Rule Alert

## Alert Observed

- Rule ID: 100100
- Alert Level: 10
- Description: Custom Alert: Multiple failed sudo login attempts detected

---

## Parent Rule

- Base Rule ID: 5503
- Description: PAM: User login failed.
- Default Level: 5

---

## Detection Engineering Logic

The custom rule uses `<if_sid>5503</if_sid>` to trigger only when the base authentication failure rule fires.

This allows severity escalation without rewriting decoders.

---

## SOC Investigation Notes

- Verified source user
- Checked timestamps
- Reviewed full log event
- Confirmed detection correlation worked correctly

---

## MITRE ATT&CK Mapping

- T1068 – Privilege Escalation

---

## Conclusion

The rule successfully escalates failed authentication attempts into high-priority alerts, demonstrating custom detection engineering capabilities.
