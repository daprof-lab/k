# 🎯 **Master File Table ($MFT)**
### `File Name: $MFT.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
The primary NTFS file system database. It contains metadata for every file and directory on an NTFS volume, including timestamps, permissions, file size, and physical cluster mapping.

---

## 🔍 **Investigative Use-Cases**
* **File Activity Mapping**: Determine when files were created, modified, accessed, or had their MFT record updated (MFT Standard Information vs File Name attributes).
* **Directory Tree Reconstruction**: Rebuild the full directory and folder structure of a suspect disk drive during forensic analysis.
* **Anomalous Executable Detection**: Identify suspicious files located in non-standard execution paths or hidden system directories.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $MFT
Author: Eric Zimmerman
Version: 1.0
Id: 2b3d01e2-25e1-4079-a630-6cb6e2069456
RecreateDirectories: true
Targets:
    -
        Name: $MFT
        Category: FileSystem
        Path: C:\
        FileMask: $MFT
        AlwaysAddToQueue: true

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/fileio/master-file-table
# https://digital-forensics.sans.org/media/DFIR-Command-Line.pdf
# https://www.andreafortuna.org/2017/10/06/macb-times-in-windows-forensic-analysis/
# https://www.andreafortuna.org/2018/06/04/using-mft-anomalies-to-spot-suspicious-files-in-forensic-analysis/
# https://www.thedigitalforensics.com/windows-forensics/timestamp-in-ntfs-system
# https://www.youtube.com/watch?v=OTea54BelTg
# https://www.sciencedirect.com/topics/computer-science/master-file-table
# https://www.tzworks.net/prototype_page.php?proto_id=46
# https://www.youtube.com/watch?v=xW5UwDztkX4
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
