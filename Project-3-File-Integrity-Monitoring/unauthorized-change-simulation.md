# 3. Unauthorized File Change Simulation

## Objective

To simulate an unauthorized modification of a critical system file and validate detection using Wazuh FIM.

---

## Target File

For this test, the `/etc/hosts` file was modified.

This file is sensitive because it controls hostname resolution on Linux systems.

---

## Simulated Unauthorized Modification

The following command was executed:

sudo echo "192.168.1.200 malicious-server" >> /etc/hosts


This simulates an attacker modifying system configuration.

---

## Expected Behavior

Wazuh FIM should detect:

- File modification event
- Hash change
- Timestamp change
- File path details
- Alert severity classification

---

## Additional Test (Optional)

To simulate further suspicious behavior:

Change file permissions:

sudo chmod 777 /etc/hosts

Or revert change after testing:

sudo chmod 644 /etc/hosts


---

## Validation in Wazuh

After modification:

1. Go to Wazuh Dashboard
2. Navigate to Security Events
3. Filter using:

or


An alert should appear indicating the file was modified.

---

## Security Context

Unauthorized modification of system configuration files is commonly associated with:

- Privilege escalation attempts
- Malware persistence
- DNS manipulation
- Lateral movement

This validates Wazuh's capability to detect integrity violations.

