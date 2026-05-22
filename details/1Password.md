# 🎯 **1password**
### `File Name: 1Password.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
1Password Password Manager

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from 1password to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate 1password events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit 1password storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: 1Password Password Manager
Author: Matt Dawson
Version: 1.0
Id: 41a37dbf-3326-4d61-a9c7-7aa38d621973
RecreateDirectories: true
Targets:
    -
        Name: 1Password Database
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\1password\data
        FileMask: '1Password10.sqlite'
        Comment: "Database which holds information about 1Password installation, such as accounts, categories, settings and more"
    -
        Name: 1Password Backup Databases
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\1password\backups
        FileMask: '1Password10.sqlite'
        Comment: "Backups of 1Password Database"
    -
        Name: 1Password Logs
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\1password\logs
        FileMask: '*.log'
        Comment: "Log of usage of 1Password - can be useful for identifying periods of user activity"

# Documentation
# https://blog.elcomsoft.com/2017/08/attacking-the-1password-master-password-follow-up/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
