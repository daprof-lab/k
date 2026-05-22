# 🎯 **Chocolatey**
### `File Name: Chocolatey.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Paul CABON (CERT CWATCH - ALMOND)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Chocolatey

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Chocolatey to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Chocolatey events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Chocolatey storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Chocolatey
Author: Paul CABON (CERT CWATCH - ALMOND)
Version: 1.0
Id: 23e556e4-614d-49c6-b2ee-bf97b1a2914b
RecreateDirectories: true
Targets:
    -
        Name: Chocolatey logs
        Category: Apps
        Path: C:\ProgramData\chocolatey\logs\
        FileMask: '*.log'
        Recursive: true

# Documentation
# https://medium.com/@stewalexander/how-to-get-chocolatey-package-manager-logs-parsed-by-the-elastic-search-elk-stack-d9bbd7d14864
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
