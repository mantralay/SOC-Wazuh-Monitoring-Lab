# 2. FIM Configuration

## Objective

To enable and verify File Integrity Monitoring (FIM) on critical system directories using Wazuh.

---

## What is FIM?

File Integrity Monitoring (FIM) tracks:

- File creation
- File modification
- File deletion
- Permission changes
- Ownership changes
- Hash changes (MD5 / SHA1 / SHA256)

This allows detection of unauthorized system changes.

---

## Default FIM Monitoring in Wazuh

By default, Wazuh monitors important directories such as:

- /etc
- /usr/bin
- /usr/sbin
- /bin
- /sbin

To verify FIM configuration:

Command: sudo nano /var/ossec/etc/ossec.conf


Look for the `<syscheck>` section.

---

## Key FIM Configuration Section

Example:

<syscheck>
  <disabled>no</disabled> 
  <frequency>3600</frequency> 
  <scan_on_start>yes</scan_on_start> 
  <directories check_all="yes">/etc</directories> 
</syscheck>

## Verifying FIM is Running
Restart Wazuh if configuration was modified:
Command: sudo systemctl restart wazuh-manager

## Check Wazuh status:
Command: sudo systemctl status wazuh-manager

FIM is now actively monitoring configured directories.
