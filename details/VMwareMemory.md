# 🎯 **VMware Guest RAM**
### `File Name: VMwareMemory.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Captures active VMware RAM snapshot files (.vmem) for memory analysis.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VMware Guest RAM to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VMware Guest RAM events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VMware Guest RAM storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VMware - Virtual Machine Memory
Author: Andrew Rathbun
Version: 1.0
Id: 45945262-2e36-47c7-a36f-3cf4124dbe63
RecreateDirectories: true
Targets:
    -
        Name: VMware (Fusion/Workstation/Server/Player)
        Category: Memory
        Path: C:\
        FileMask: '*.vmem'
        Recursive: true
        Comment: "Captures all raw memory from VMware virtual machines."
    -
        Name: VMware (Fusion/Workstation/Server/Player)
        Category: Memory
        Path: C:\
        FileMask: '*.vmss'
        Recursive: true
        Comment: "Captures all memory images from VMware virtual machines."
    -
        Name: VMware (Fusion/Workstation/Server/Player)
        Category: Memory
        Path: C:\
        FileMask: '*.vmsn'
        Recursive: true
        Comment: "Captures all memory images from VMware virtual machines."

# Documentation
# https://crucialsecurity.wordpress.com/2011/05/23/virtual-machine-files-essential-to-forensic-investigations/
# https://blog.salvationdata.com/2018/06/01/case-study-how-to-forensically-extract-evidence-data-from-a-virtual-machine/
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
