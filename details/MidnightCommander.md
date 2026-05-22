# 🎯 **Midnight Commander**
### `File Name: MidnightCommander.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Midnight Commander

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Midnight Commander to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Midnight Commander events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Midnight Commander storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Midnight Commander
Author: Andrew Rathbun
Version: 1.0
Id: c02a2310-8ec2-4c0f-8a8a-b20ac0820e46
RecreateDirectories: true
Targets:
    -
        Name: Midnight Commander -- All Configuation Files
        Category: Apps
        Path: C:\Users\%user%\Midnight Commander\
        Comment: "Locates folder where all configuration files reside"

# Documentation
# https://midnight-commander.org/
# Midnight Commander is a free, open course orthodox file manager similar to Norton Commander.
# This folder is created upon install so it should be where all configuration files resides. I've not done extensive testing on this one due to the DOSness of the application.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
