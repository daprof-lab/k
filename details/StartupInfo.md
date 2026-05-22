# 🎯 **Startup Info**
### `File Name: StartupInfo.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Hadar Yudovich  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
StartupInfo XML Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Startup Info to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Startup Info events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Startup Info storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: StartupInfo XML Files
Author: Hadar Yudovich
Version: 1.0
Id: 9bb477a3-fa6f-410d-8646-c3f987c147ce
RecreateDirectories: true
Targets:
    -
        Name: StartupInfo XML Files
        Category: Persistence
        Path: C:\Windows\System32\WDI\LogFiles\StartupInfo\
        FileMask: '*.xml'
    -
        Name: StartupInfo XML Files
        Category: Persistence
        Path: C:\Windows.old\Windows\System32\WDI\LogFiles\StartupInfo\
        FileMask: '*.xml'

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
