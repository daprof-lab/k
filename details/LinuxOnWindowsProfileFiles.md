# 🎯 **Linux On Windows Profile Files**
### `File Name: LinuxOnWindowsProfileFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Troy Larson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Linux on Windows Profile Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Linux On Windows Profile Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Linux On Windows Profile Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Linux On Windows Profile Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Linux on Windows Profile Files
Author: Troy Larson
Version: 1.0
Id: 9718a129-21f9-4354-a06f-2eddb112ab03
RecreateDirectories: true
Targets:
    -
        Name: .bash_history
        Category: Windows Linux Profile
        Path: C:\Users\%user%\AppData\Local\Packages\*\LocalState\rootfs\home\*\
        FileMask: '.bash_history'
    -
        Name: .bash_logout
        Category: Windows Linux Profile
        Path: C:\Users\%user%\AppData\Local\Packages\*\LocalState\rootfs\home\*\
        FileMask: '.bash_logout'
    -
        Name: .bashrc
        Category: Windows Linux Profile
        Path: C:\Users\%user%\AppData\Local\Packages\*\LocalState\rootfs\home\*\
        FileMask: '.bashrc'
    -
        Name: .profile
        Category: Windows Linux Profile
        Path: C:\Users\%user%\AppData\Local\Packages\*\LocalState\rootfs\home\*\
        FileMask: '.profile'

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
