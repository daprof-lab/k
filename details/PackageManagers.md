# 🎯 **Package Managers**
### `File Name: PackageManagers.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Paul CABON (CERT CWATCH - ALMOND)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Compound Target for files related to package managers

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Package Managers to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Package Managers events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Package Managers storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Compound Target for files related to package managers
Author: Paul CABON (CERT CWATCH - ALMOND)
Version: 1.0
Id: 5ccfa226-5cff-48d8-b6ef-46e050001f17
RecreateDirectories: true
Targets:
    -
        Name: Chocolatey
        Category: ApplicationLogs
        Path: Chocolatey.tkape

# Documentation
# Collecting different artifacts related to package managers
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
