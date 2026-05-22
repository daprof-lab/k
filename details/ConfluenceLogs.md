# 🎯 **Confluence Logs**
### `File Name: ConfluenceLogs.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Eric Capuano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Confluence Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Confluence Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Confluence Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Confluence Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Confluence Log Files
Author: Eric Capuano
Version: 1.0
Id: 317b3814-b383-4bcf-97a2-3b3d1c5f8ca0
RecreateDirectories: true
Targets:
    -
        Name: Confluence Wiki Log Files
        Category: Logs
        Path: C:\Atlassian\Application Data\Confluence\logs\
        FileMask: '*.log*'
    -
        Name: Confluence Wiki Log Files
        Category: Logs
        Path: C:\Program Files\Atlassian\Confluence\logs\
        FileMask: '*.log'

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
