# 🎯 **Recycle Bin Data Files**
### `File Name: RecycleBin_DataFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Joshua Hickman, Andreas Hunkeler (@Karneades), Brian Maloney  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Recycle Bin Data Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Recycle Bin Data Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Recycle Bin Data Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Recycle Bin Data Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Recycle Bin Data Files
Author: Joshua Hickman, Andreas Hunkeler (@Karneades), Brian Maloney
Version: 1.2
Id: bb5785ec-0e6e-42f9-97ca-94ef12720827
RecreateDirectories: true
Targets:
    -
        Name: Recycle Bin - Windows Vista+
        Category: FileDeletion
        Path: C:\$Recycle.Bin\
        FileMask: '$R*'
        Recursive: true
    -
        Name: Recycle Bin - Windows Vista+
        Category: FileDeletion
        Path: C:\$Recycle.Bin\*\$R*\
        Recursive: true
    -
        Name: RECYCLER - WinXP
        Category: FileDeletion
        Path: C:\RECYCLE*\
        FileMask: 'D*'
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
