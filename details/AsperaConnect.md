# 🎯 **Aspera Connect**
### `File Name: AsperaConnect.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Dennis Reneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Aspera Connect Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Aspera Connect to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Aspera Connect events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Aspera Connect storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Aspera Connect Log Files
Author: Dennis Reneau
Version: 1.0
Id: 1f311765-a5c0-496a-a5d5-e79cbd0702e2
RecreateDirectories: true
Targets:
    -
        Name: Aspera Client Logs
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Aspera\Aspera Connect\var\log\
        FileMask: '*.log'
        Recursive: true
    -
        Name: Aspera Server Logs
        Category: FileDownload
        Path: C:\Users\%user%\.aspera\connect\var\log\
        FileMask: '*.log'
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
