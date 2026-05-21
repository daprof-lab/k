# 🎯 **Recycle Bin Metadata**
### `File Name: RecycleBin.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mark Hallman / Joshua Hickman  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Deleted file metadata files ($I*) and raw deleted file contents ($R*) residing within the hidden `$Recycle.Bin` directory on all drives.

---

## 🔍 **Investigative Use-Cases**
* **Deleted Files Auditing**: Retrieve the original file names, deletion times, and original paths of files deleted via the GUI Recycle Bin.
* **Data Exfiltration Detection**: Verify if files were deleted shortly after USB device connections or web uploads, suggesting exfiltration cleanup.
* **Evidence Recovery**: Reconstruct and recover the original contents of deleted folders and documents.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Recycle Bin DataAndInfo
Author: Mark Hallman / Joshua Hickman
Version: 2.0
Id: afac78f5-a5bc-475d-9c67-649456dc4dc2
RecreateDirectories: true
Targets:
    -
        Name: RecycleBin_InfoFiles
        Category: FileDeletion
        Path: RecycleBin_InfoFiles.tkape
    -
        Name: RecycleBin_DataFiles
        Category: FileDeletion
        Path: RecycleBin_DataFiles.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
