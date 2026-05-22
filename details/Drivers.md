# 🎯 **Drivers**
### `File Name: Drivers.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Zawadi Done  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Drivers

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Drivers to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Drivers events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Drivers storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Drivers
Author: Zawadi Done
Version: 1.0
Id: fc56e4eb-c9e6-481f-9f57-6b24ba8bcbfb
RecreateDirectories: true
Targets:
    -
        Name: Drivers
        Category: Drivers
        Path: C:\Windows\system32\drivers\
        FileMask: '*.sys'
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
