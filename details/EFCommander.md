# 🎯 **Efcommander**
### `File Name: EFCommander.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
EF Commander

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Efcommander to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Efcommander events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Efcommander storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: EF Commander
Author: Andrew Rathbun
Version: 1.0
Id: e94a00dd-3206-4a2c-aa5c-a69f7a09b7b3
RecreateDirectories: true
Targets:
    -
        Name: EF Commander - .ini File
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\EFSoftware\
        Comment: "Locates folder where all configuration files reside"

# Documentation
# http://www.efsoftware.com/cw/e.htm
# EF Commander is a shareware file manager similar to Total Commander.
# EFCW.INI will have the history of the left and right panel as well as any FTP servers the user connected to.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
