# 🎯 **mIRC Chat Client**
### `File Name: mIRC.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Configuration files, transfer records, and chat logging files from the classic mIRC client.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from mIRC Chat Client to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate mIRC Chat Client events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit mIRC Chat Client storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: mIRC
Author: Andrew Rathbun
Version: 1.0
Id: 284ffb97-076c-4990-b10a-044d40ac1901
RecreateDirectories: true
Targets:
    -
        Name: mIRC Chat Logs (Vista+)
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\mIRC\logs\
        Recursive: true
    -
        Name: mIRC Chat Logs (2000/XP)
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\mIRC\logs\
        Recursive: true

# Documentation
# https://ir3e.com/chapter-14-additional-im-clients/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
