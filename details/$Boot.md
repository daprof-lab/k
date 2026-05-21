# 🎯 **Volume Boot Record ($Boot)**
### `File Name: $Boot.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
The boot sector of an NTFS partition. It contains crucial disk geometry configurations, cluster sizing, and bootstrap code used by the system bootloader.

---

## 🔍 **Investigative Use-Cases**
* **Disk Geometry Validation**: Verify partition structures, sector sizes, and boot flags to ensure accurate raw image parsing.
* **Bootkit Anomaly Detection**: Inspect bootloader sectors for boot-level malware, rootkits, or unauthorized changes to the active boot code.
* **File System Identification**: Confirm file system architecture and cluster settings during partition-level forensics.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $Boot
Author: Eric Zimmerman
Version: 1.0
Id: 9f24d727-fcf0-492d-97cc-108472eb4e00
RecreateDirectories: true
Targets:
    -
        Name: $Boot
        Category: FileSystem
        Path: C:\
        FileMask: $Boot
        AlwaysAddToQueue: true

# Documentation
# https://digital-forensics.sans.org/media/DFIR-Command-Line.pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
