# 🎯 **Hex Chat**
### `File Name: HexChat.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
HexChat

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Hex Chat to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Hex Chat events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Hex Chat storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: HexChat
Author: Andrew Rathbun
Version: 1.0
Id: a26181fc-1931-4d48-9b5d-44f6f8f71ccc
RecreateDirectories: true
Targets:
    -
        Name: HexChat Chat Logs
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\HexChat\logs\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
