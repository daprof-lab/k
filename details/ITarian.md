# 🎯 **Itarian**
### `File Name: ITarian.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ITarian RMM

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Itarian to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Itarian events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Itarian storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ITarian RMM
Author: Phill Moore
Version: 1.0
Id: aa387dbf-3326-a9c7-4d61-7d62197341a3
RecreateDirectories: true
Targets:
    -
        Name: ITarian
        Category: Apps
        Path: C:\Program Files\ITarian\Endpoint Manager\rmmlogs
        Comment: ""
    -
        Name: ITarian
        Category: Apps
        Path: C:\Program Files (x86)\ITarian\Endpoint Manager\rmmlogs
        Comment: ""
    -
        Name: Comodo
        Category: Apps
        Path: C:\Program Files\Comodo\Endpoint Manager\rmmlogs
        Comment: ""
    -
        Name: ITarian
        Category: Apps
        Path: C:\Program Files (x86)\Comodo\Endpoint Manager\rmmlogs
        Comment: ""

# Documentation
# https://russianpanda.com/The-Abuse-of-ITarian-RMM-by-Dolphin-Loader
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
