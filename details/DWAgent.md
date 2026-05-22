# 🎯 **Dwagent**
### `File Name: DWAgent.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ron Rader  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
DWAgent Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Dwagent to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Dwagent events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Dwagent storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: DWAgent Log Files
Author: Ron Rader
Version: 1.0
Id: e78d2652-df47-4edc-a0ea-4835c322ad48
RecreateDirectories: true
Targets:
    -
        Name: DWAgent Log Files
        Category: Logs
        Path: C:\ProgramData\DWAgent*\
        FileMask: '*.log*'

# Documentation
# https://www.dwservice.net/en/faq.html
# https://github.com/AG7GN/dwservice/blob/master/README.md
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
