# 🎯 **SDB**
### `File Name: SDB.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Troy Larson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Shim SDB FIles

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from SDB to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate SDB events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit SDB storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Shim SDB FIles
Author: Troy Larson
Version: 1.0
Id: 99e82a85-e4d4-4139-930c-7eea9a45452f
RecreateDirectories: true
Targets:
    -
        Name: SDB Files
        Category: Executables
        Path: C:\Windows\apppatch\Custom\
        FileMask: '*.sdb'
    -
        Name: SDB Files
        Category: Executables
        Path: C:\Windows.old\Windows\apppatch\Custom\
        FileMask: '*.sdb'
    -
        Name: SDB Files x64
        Category: Executables
        Path: C:\Windows\apppatch\Custom\Custom64\
        FileMask: '*.sdb'
    -
        Name: SDB Files x64
        Category: Executables
        Path: C:\Windows.old\Windows\apppatch\Custom\Custom64\
        FileMask: '*.sdb'

# Documentation
# https://geoffchappell.com/studies/windows/win32/apphelp/sdb/index.htm?tx=54
# https://docs.microsoft.com/en-us/windows/win32/devnotes/application-compatibility-database?redirectedfrom=MSDN
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
