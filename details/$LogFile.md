# 🎯 **NTFS Transaction Log ($LogFile)**
### `File Name: $LogFile.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
A transaction log used by NTFS to maintain file system integrity. It records transaction steps for metadata operations before they are committed to the MFT.

---

## 🔍 **Investigative Use-Cases**
* **High-Fidelity Transaction Recovery**: Recover highly volatile transaction histories for very recent file deletions or directory creations.
* **Incident Timeline Synchronization**: Analyze micro-second sequences of file metadata updates to coordinate an attack timeline.
* **Deleted Data Location**: Retrieve filenames and parent records that were deleted shortly before power loss or system shutdown.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $LogFile
Author: Eric Zimmerman
Version: 1.0
Id: b98612e0-f679-400a-954f-c0b2bc86147b
RecreateDirectories: true
Targets:
    -
        Name: $LogFile
        Category: FileSystem
        Path: C:\
        FileMask: $LogFile
        AlwaysAddToQueue: true

# Documentation
# https://link.springer.com/chapter/10.1007/978-3-642-35515-8_18
# https://digital-forensics.sans.org/summit-archives/DFIR_Summit/File-System-Journaling-Forensics-Theory-Procedures-and-Analysis-Impacts-David-Cowen-with-Matthew-Seyer.pdf
# https://dfir.ru/2019/02/16/how-the-logfile-works/
# https://countuponsecurity.com/tag/ntfs-logfile/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
