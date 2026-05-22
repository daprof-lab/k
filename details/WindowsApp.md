# 🎯 **Windows App**
### `File Name: WindowsApp.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WindowsApp Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows App to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows App events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows App storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: WindowsApp Logs
Author: Vito Alfano
Version: 1.0
Id: 11bef2d8-39b2-4fc8-b81e-9bbe177fcf63
RecreateDirectories: true
Targets:
    -
        Name: WindowsApp
        Category: EventLogs
        Path: C:\Users\*\AppData\Local\Temp\DiagOutputDir\Windows365\
        Recursive: true

# Documentation
# https://learn.microsoft.com/en-us/windows-app/admins/troubleshoot-collect-logs
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
