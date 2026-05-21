# 🎯 **VirtualBox RAM**
### `File Name: VirtualBoxMemory.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Volatile memory dumps, guest OS configurations, and runtime state records for VirtualBox.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VirtualBox RAM to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VirtualBox RAM events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VirtualBox RAM storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VirtualBox - Memory
Author: Andrew Rathbun
Version: 1.0
Id: 4af61e3f-7fa7-4c59-a6d7-a495582fbb56
RecreateDirectories: true
Targets:
    -
        Name: VirtualBox
        Category: Memory
        Path: C:\
        FileMask: '*.sav'
        Recursive: true
        Comment: "Captures all partial memory images from VirtualBox."

# Documentation
# https://www.researchgate.net/publication/323676948_Virtual_Machine_Forensic_Analysis_And_Recovery_Method_For_Recovery_And_Analysis_Digital_Evidence
# https://www.researchgate.net/publication/323676948_Virtual_Machine_Forensic_Analysis_And_Recovery_Method_For_Recovery_And_Analysis_Digital_Evidence
# https://digitalforensicsurvivalpodcast.com/2017/04/25/dfsp-062-building-a-forensic-vm-with-virtualbox/
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
