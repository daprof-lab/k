# 🎯 **Program Data**
### `File Name: ProgramData.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ProgramData Folder Copy

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Program Data to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Program Data events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Program Data storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ProgramData Folder Copy
Author: Vito Alfano
Version: 1.0
Id: 4f1c3500-57cf-4c34-9ede-434c193a2c77
RecreateDirectories: true
Targets:
    -
        Name: ProgramData
        Category: ApplicationData
        Path: C:\ProgramData\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
