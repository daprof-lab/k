# 🎯 **Exchange Client Access**
### `File Name: ExchangeClientAccess.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Keith Twombley  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Exchange Client Access Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Exchange Client Access to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Exchange Client Access events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Exchange Client Access storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Exchange Client Access Log Files
Author: Keith Twombley
Version: 1.0
Id: 9e802154-53eb-4cc9-9cca-d2e39f3227d7
RecreateDirectories: true
Targets:
    -
        Name: Exchange client access log files
        Category: Logs
        Path: C:\Program Files\Microsoft\Exchange Server\*\Logging\
        Recursive: true
        FileMask: '*.log'
        Comment: "Highly dependent on Exchange configuration"

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
