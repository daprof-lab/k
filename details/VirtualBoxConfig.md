# 🎯 **Virtual Box Config**
### `File Name: VirtualBoxConfig.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects VirtualBox configuration files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Virtual Box Config to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Virtual Box Config events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Virtual Box Config storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collects VirtualBox configuration files
Author: Matt Dawson
Version: 1.0
Id: 0983f8c9-721b-4dd5-b4d2-f16ee289b1c3
RecreateDirectories: true
Targets:
    -
        Name: VirtualBox VM configs
        Category: Apps
        Path: C:\
        Recursive: true
        FileMask: "*.vbox"
        Comment: "Locates all .vbox VM configuration files on disk"
    -
        Name: VirtualBox VM backup configs
        Category: Apps
        Path: C:\
        Recursive: true
        FileMask: "*.vbox-prev"
        Comment: "Locates all backup .vbox VM configuration files on disk"

# Documentation
# N/A
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
