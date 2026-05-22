# 🎯 **Speed Commander**
### `File Name: SpeedCommander.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SpeedCommander

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Speed Commander to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Speed Commander events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Speed Commander storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SpeedCommander
Author: Andrew Rathbun
Version: 1.0
Id: 237f2355-4ae1-4461-812f-2833003aabc3
RecreateDirectories: true
Targets:
    -
        Name: SpeedCommander - .ini File
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\SpeedProject\SpeedCommander 19\
        Comment: "Locates folder where all configuration files reside"

# Documentation
# https://www.speedproject.com/
# SpeedCommander is a shareware file manager similar to Total Commander.
# SpeedCommander.xml will have the history of the left and right panel as well as any FTP servers the user connected to.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
