# 🎯 **Ammyy Admin**
### `File Name: Ammyy.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Configuration parameters, server records, and connection diaries from Ammyy Admin.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Ammyy Admin to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Ammyy Admin events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Ammyy Admin storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Ammyy Data
Author: Drew Ervin
Version: 1.0
Id: 606ad937-c32e-49ba-9403-3f1ce501a012
RecreateDirectories: true
Targets:
    -
        Name: Ammyy Program Data
        Category: ApplicationLogs
        Path: C:\ProgramData\Ammyy\
        Recursive: true
        Comment: "May not contain traditional log files, but presence of this folder may indicate historical usage"

# Documentation
# N/A
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
