# 🎯 **Zscaler**
### `File Name: ZScaler.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Zscaler Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Zscaler to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Zscaler events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Zscaler storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Zscaler Logs
Author: Vito Alfano
Version: 1.0
Id: 0f3c8e4c-2307-4dcf-846b-17a888a585a6
RecreateDirectories: true
Targets:
    -
        Name: Zscaler Logs
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Local\Zscaler
        FileMask: '*'
        Comment: "Contains Zscaler agent Logs entries"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
