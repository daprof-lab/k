# 🎯 **Level**
### `File Name: Level.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Skatoff @DFIR_TNT  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Level.io Application Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Level to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Level events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Level storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Level.io Application Logs
Author: Andrew Skatoff @DFIR_TNT
Version: 1.1
Id: 27ad29e0-13a8-11f0-8533-1faa3a27bf6a
RecreateDirectories: true
Targets:
    -
        Name: Level RMM Client Application logs
        Category: ApplicationLogs
        Path: C:\Program Files\Level
        FileMask: '*.log'
        Comment: "Contains Application Log entries such as service start and incoming connections."

# Documentation
# https://www.crowdstrike.com/blog/analysis-of-intrusion-campaign-targeting-telecom-and-bpo-companies/
# https://dfirtnt.wordpress.com/2023/09/05/rmm-level-io-forensic-artifacts-and-evidence/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
