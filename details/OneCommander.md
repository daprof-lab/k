# 🎯 **One Commander**
### `File Name: OneCommander.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
One Commander

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from One Commander to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate One Commander events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit One Commander storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: One Commander
Author: Andrew Rathbun
Version: 1.0
Id: 5b532f4e-f6cb-4d59-bd44-91b9f9d94a54
RecreateDirectories: true
Targets:
    -
        Name: One Commander - All Configuration Files
        Category: Apps
        Path: C:\Users\%user%\OneCommander\
        Comment: "Locates folder where all configuration files reside"
    -
        Name: One Commander - Other Configuration Files
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Apps\2.0\*\*\onec*\
        Recursive: true
        Comment: "Locates folder where all configuration files reside"

# Documentation
# https://onecommander.com/
# One Commander is a freeware file manager similar to Total Commander.
# \%user%\OneCommander\Logs\OCLog20210404.txt will have a play by play of user activity, however, it doesn't appear to be as verbose as one would expect. I've yet to see exact folder paths specified within this file in my limited testing.
# .\%user\OneCommander\Settings\OneCommanderV3.json will have the name of the user's PC.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
