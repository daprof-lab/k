# 🎯 **VMware VM Inventory**
### `File Name: VMwareInventory.tkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Inventory configurations, VM structures, and registration tables for VMware instances.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VMware VM Inventory to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VMware VM Inventory events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VMware VM Inventory storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VMware - Virtual Machine Inventory
Author: Andrew Rathbun
Version: 1.0
Id: 92d4917d-54a3-48a1-873b-ea2ddad58b84
RecreateDirectories: true
Targets:
    -
        Name: VMware - Virtual Machine Inventory
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\VMware
        Comment: "Locates an inventory of all Virtual Machines on disk."

# Documentation
# https://crucialsecurity.wordpress.com/2011/05/23/virtual-machine-files-essential-to-forensic-investigations/
# https://blog.salvationdata.com/2018/06/01/case-study-how-to-forensically-extract-evidence-data-from-a-virtual-machine/
# VMware Workstation Pro stores a file named inventory.vmls which will provide file paths to Virtual Machines located on the user's system.
# Important evidence could be located within these Virtual Machines so this is great information to know.
# Preferences.ini will provide other file paths relating to the existing Virtual Machines on the user's system.
# Inventory.vmls can be viewed in any text editor and provides similar information to Preferences.ini.
```
---

[⬅️ Back to Memory & Virtualization Targets](../memory_virtualization_targets.md)
