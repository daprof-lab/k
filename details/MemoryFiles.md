# 🎯 **System Memory Dumps**
### `File Name: MemoryFiles.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Ahmed Elshaer / Teo Kia Meng  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Automatically targets physical memory dumps, crashdumps, and active swap/page files on disk.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from System Memory Dumps to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate System Memory Dumps events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit System Memory Dumps storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Memory Files
Author: Ahmed Elshaer, Teo Kia Meng
Version: 1.0
Id: d9e7fc93-7b63-4286-aa05-27ce3437c9c0
RecreateDirectories: true
Targets:
    -
        Name: hiberfil.sys
        Category: Memory
        Path: C:\
        FileMask: hiberfil.sys
        AlwaysAddToQueue: true
    -
        Name: pagefile.sys
        Category: Memory
        Path: C:\
        FileMask: pagefile.sys
        AlwaysAddToQueue: true
    -
        Name: swapfile.sys
        Category: Memory
        Path: C:\
        FileMask: swapfile.sys
        AlwaysAddToQueue: true
    -
        Name: Small Memory Dump directory
        Category: Memory
        Path: C:\Windows\Minidump\
        FileMask: '*.dmp'
        Comment: "https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/small-memory-dump"
    -
        Name: Small Memory Dump directory
        Category: Memory
        Path: C:\Windows.old\Windows\Minidump\
        FileMask: '*.dmp'
        Comment: "https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/small-memory-dump"

# Documentation
# https://www.13cubed.com/episodes/memory.html
# https://digital-forensics.sans.org/media/volatility-memory-forensics-cheat-sheet.pdf
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
