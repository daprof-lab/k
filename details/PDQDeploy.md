# 🎯 **Pdqdeploy**
### `File Name: PDQDeploy.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Paul Cabon - Cwatch CERT Almond  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PDQ Deploy database

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Pdqdeploy to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Pdqdeploy events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Pdqdeploy storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: PDQ Deploy database
Author: Paul Cabon - Cwatch CERT Almond
Version: 1.0
Id: 5f388422-ce52-45e8-b1a5-4d7300660439
RecreateDirectories: true
Targets:
    -
        Name: PDQ Deploy database
        Category: Database
        Path: C:\ProgramData\Admin Arsenal\PDQ Deploy\
        FileMask: '*.db'

# Documentation
# https://thedfirreport.com/2025/02/24/confluence-exploit-leads-to-lockbit-ransomware/
# https://documentation.pdq.com/PDQDeploy/19.3.409.0/index.html?pdq-deploy-database.htm
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
