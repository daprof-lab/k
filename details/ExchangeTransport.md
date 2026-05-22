# 🎯 **Exchange Transport**
### `File Name: ExchangeTransport.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Keith Twombley  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Exchange Transport Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Exchange Transport to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Exchange Transport events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Exchange Transport storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Exchange Transport Log Files
Author: Keith Twombley
Version: 1.0
Id: 9bc0a453-50ab-46e8-a424-09dc7022c4a4
RecreateDirectories: true
Targets:
    -
        Name: Exchange TransportRoles log files
        Category: Logs
        Path: C:\Program Files\Microsoft\Exchange Server\*\TransportRoles\Logs\
        Recursive: true
        FileMask: '*.log'
        Comment: "Highly dependent on Exchange configuration"

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
