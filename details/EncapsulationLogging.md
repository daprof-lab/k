# 🎯 **Encapsulation Logging**
### `File Name: EncapsulationLogging.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Troy Larson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
EncapsulationLogging

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Encapsulation Logging to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Encapsulation Logging events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Encapsulation Logging storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: EncapsulationLogging
Author: Troy Larson
Version: 1.0
Id: 7c328d9b-4a10-459d-b8b3-36d81686bc74
RecreateDirectories: true
Targets:
    -
        Name: EncapsulationLogging
        Category: Executables
        Path: C:\Windows\Appcompat\Programs\
        FileMask: EncapsulationLogging.hve
    -
        Name: EncapsulationLogging
        Category: Executables
        Path: C:\Windows.old\Windows\Appcompat\Programs\
        FileMask: EncapsulationLogging.hve
    -
        Name: EncapsulationLogging Logs
        Category: Executables
        Path: C:\Windows\Appcompat\Programs\
        FileMask: EncapsulationLogging.hve.log*
    -
        Name: EncapsulationLogging Logs
        Category: Executables
        Path: C:\Windows.old\Windows\Appcompat\Programs\
        FileMask: EncapsulationLogging.hve.log*

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
