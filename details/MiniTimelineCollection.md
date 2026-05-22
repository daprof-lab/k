# 🎯 **Mini Timeline Collection**
### `File Name: MiniTimelineCollection.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Mari DeGrazia  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFT, Registry and Event Logs to generate a mini timeline

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mini Timeline Collection to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mini Timeline Collection events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mini Timeline Collection storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MFT, Registry and Event Logs to generate a mini timeline
Author: Mari DeGrazia
Version: 1.0
Id: 02e131d6-7784-4302-9495-75536423e414
RecreateDirectories: true
Targets:
    -
        Name: Event Logs
        Category: EventLogs
        Path: EventLogs.tkape
    -
        Name: File System
        Category: FileSystem
        Path: FileSystem.tkape
    -
        Name: RegistryHives
        Category: Registry
        Path: RegistryHives.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
