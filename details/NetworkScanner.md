# 🎯 **Network Scanner**
### `File Name: NetworkScanner.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Reece394  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Network Scanner Tools

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Network Scanner to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Network Scanner events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Network Scanner storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Network Scanner Tools
Author: Reece394
Version: 1.0
Id: 07b4d985-3314-4814-b200-4d5ef92f455c
RecreateDirectories: true
Targets:
    -
        Name: Advanced IP Scanner
        Category: Apps
        Path: AdvancedIPScanner.tkape
    -
        Name: Advanced Port Scanner
        Category: Apps
        Path: AdvancedPortScanner.tkape
    -
        Name: Soft Perfect Network Scanner
        Category: Apps
        Path: SoftPerfectNetscan.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
