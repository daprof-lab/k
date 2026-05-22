# 🎯 **Virtual Box**
### `File Name: VirtualBox.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs all VirtualBox modules to collect Virtualbox VM config files, logs and Virtual Hard Disks

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Virtual Box to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Virtual Box events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Virtual Box storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Runs all VirtualBox modules to collect Virtualbox VM config files, logs and Virtual Hard Disks
Author: Matt Dawson
Version: 1.0
Id: b6ce74ad-11a1-4e3c-851e-f8772749894b
RecreateDirectories: true
Targets:
    -
        Name: VirtualBox Logs
        Category: Apps
        Path: VirtualBoxLogs.tkape
    -
        Name: VirtualBox Memory
        Category: Apps
        Path: VirtualBoxMemory.tkape
    -
        Name: VirtualBox Configs
        Category: Apps
        Path: VirtualBoxConfig.tkape
    -
        Name: Virtual Hard Drives
        Category: Apps
        Path: VirtualDisks.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
