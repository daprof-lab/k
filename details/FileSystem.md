# 🎯 **Master File System Triage**
### `File Name: FileSystem.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers all MFT, logfile, boot, and volume transactional logs in a single collection.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Master File System Triage to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Master File System Triage events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Master File System Triage storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: File system metadata
Author: Eric Zimmerman
Version: 1.0
Id: 2bd97ef7-5fbf-4427-8ca2-ffb15d545b00
RecreateDirectories: true
Targets:
    -
        Name: $MFT
        Category: FileSystem
        Path: $MFT.tkape
    -
        Name: $LogFile
        Category: FileSystem
        Path: $LogFile.tkape
    -
        Name: $J
        Category: FileSystem
        Path: $J.tkape
    -
        Name: $SDS
        Category: FileSystem
        Path: $SDS.tkape
    -
        Name: $Boot
        Category: FileSystem
        Path: $Boot.tkape
    -
        Name: $T
        Category: FileSystem
        Path: $T.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
