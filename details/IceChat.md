# 🎯 **Ice Chat**
### `File Name: IceChat.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IceChat

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Ice Chat to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Ice Chat events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Ice Chat storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IceChat
Author: Andrew Rathbun
Version: 1.0
Id: 4c437510-9fba-4d36-8070-0a14c29f1033
RecreateDirectories: true
Targets:
    -
        Name: IceChat Chat Logs
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\IceChat Networks\IceChat\Logs\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
