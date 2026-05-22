# 🎯 **Total AV**
### `File Name: TotalAV.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Kirtan Shah  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
TotalAV Antivirus Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Total AV to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Total AV events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Total AV storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: TotalAV Antivirus Data
Author: Kirtan Shah
Version: 1.0
Id: 8e5ca015-26e8-4993-8008-19421d15f35a
RecreateDirectories: true
Targets:
    -
        Name: TotalAV Logs
        Category: Antivirus
        Path: C:\Program Files*\TotalAV\logs
        Recursive: true
    -
        Name: TotalAV Logs
        Category: Antivirus
        Path: C:\ProgramData\TotalAV\logs
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
