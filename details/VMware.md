# 🎯 **Vmware**
### `File Name: VMware.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs all VMware modules to collect VMware VM config files, logs and Virtual Hard Disks

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Vmware to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Vmware events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Vmware storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Runs all VMware modules to collect VMware VM config files, logs and Virtual Hard Disks
Author: Matt Dawson
Version: 1.0
Id: 386c40b5-8fc4-495e-b34e-47508e6c3f73
RecreateDirectories: true
Targets:
    -
        Name: VMware Inventory
        Category: Apps
        Path: VMwareInventory.tkape
    -
        Name: VMware Memory
        Category: Apps
        Path: VMwareMemory.tkape
    -
        Name: Virtual Hard Drives
        Category: Apps
        Path: VirtualDisks.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
