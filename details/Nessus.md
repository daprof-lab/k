# 🎯 **Nessus**
### `File Name: Nessus.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Nessus

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Nessus to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Nessus events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Nessus storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Nessus
Author: Andrew Rathbun
Version: 1.0
Id: eceacdb8-28ac-4ddd-8214-a52deee12c7f
RecreateDirectories: true
Targets:
    -
        Name: Nessus Logs
        Category: Nessus
        Path: C:\ProgramData\Tenable\Nessus\conf
        Recursive: true
        Comment: ""
    -
        Name: Nessus Logs
        Category: Nessus Logs
        Path: C:\ProgramData\Tenable\Nessus\nessus\logs\
        Recursive: true
        Comment: ""

# Documentation
# The following files of interest are stored in the above locations. Currently, it is unknown if any other files of interest exist in these locations.
# C:\ProgramData\Tenable\Nessus\conf\nessusd.rules
# C:\ProgramData\Tenable\Nessus\nessus\logs\nessusd.dumpa
# C:\ProgramData\Tenable\Nessus\nessus\logs\www_server.log
# C:\ProgramData\Tenable\Nessus\nessus\logs\nessusd.messages
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
