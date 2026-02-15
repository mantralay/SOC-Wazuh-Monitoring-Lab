# 3. Custom Rule Creation

## Objective

To create a custom Wazuh rule that detects repeated failed sudo authentication attempts.

---

## Rule Design Strategy

We identified from logs that failed sudo attempts contain:

- "sudo"
- "authentication failure"
- "incorrect password attempts"

We will create a rule that triggers when:

- Multiple failed sudo attempts occur
- Pattern matches authentication failure message

---

## Custom Rule Location

Custom rules are stored in:

/var/ossec/etc/rules/local_rules.xml


---

## Creating the Custom Rule

Open the file:

sudo nano /var/ossec/etc/rules/local_rules.xml


Add the following rule inside the `<rules>` section:

```xml
<group name="sudo,custom,">
  <rule id="100100" level="10">
    <if_sid>5402</if_sid>
    <match>authentication failure</match>
    <description>Custom Alert: Multiple failed sudo authentication attempts detected</description>
    <mitre>
      <id>T1068</id>
    </mitre>
  </rule>
</group>

