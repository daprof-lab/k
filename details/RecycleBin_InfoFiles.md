# 🎯 **Recycle Bin Info Files**
### `File Name: RecycleBin_InfoFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Joshua Hickman, Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Recycle Bin Info Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Recycle Bin Info Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Recycle Bin Info Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Recycle Bin Info Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Recycle Bin Info Files
Author: Joshua Hickman, Andreas Hunkeler (@Karneades)
Version: 1.0
Id: 6205454f-fcaa-4ace-a7b5-33c4e40b156a
RecreateDirectories: true
Targets:
    -
        Name: Recycle Bin - Windows Vista+
        Category: FileDeletion
        Path: C:\$Recycle.Bin\
        FileMask: '$I*'
        Recursive: true
    -
        Name: RECYCLER - WinXP
        Category: FileDeletion
        Path: C:\RECYCLE*\
        FileMask: 'INFO2'
        Recursive: true

# Documentation
# https://www.youtube.com/watch?v=Gkir-wGqG2c
# https://www.andreafortuna.org/2019/09/26/windows-forensics-analysis-of-recycle-bin-artifacts/
# https://www.blackbagtech.com/blog/examining-the-windows-10-recycle-bin/
# https://www.sans.org/security-resources/posters/windows-forensics-evidence-of/75/download
# https://dereknewton.com/2010/06/recycle-bin-forensics-in-windows-7-and-vista/
# https://www.forensafe.com/blogs/recyclebin.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
