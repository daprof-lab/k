# 🎯 **Virtual Disks**
### `File Name: VirtualDisks.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Virtual Disks

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Virtual Disks to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Virtual Disks events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Virtual Disks storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Virtual Disks
Author: Phill Moore
Version: 1.0
Id: 283fd2b7-b914-4683-85b4-40dd3fefecbb
RecreateDirectories: true
Targets:
    -
        Name: VHD
        Category: Disk Images
        Path: C:\
        FileMask: '*.VHD'
        Recursive: true
    -
        Name: VHDX
        Category: Disk Images
        Path: C:\
        FileMask: '*.VHDX'
        Recursive: true
    -
        Name: VDI
        Category: Disk Images
        Path: C:\
        FileMask: '*.VDI'
        Recursive: true
    -
        Name: VMDK
        Category: Disk Images
        Path: C:\
        FileMask: '*.VMDK'
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
