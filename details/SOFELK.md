# 🎯 **SOFELK**
### `File Name: SOFELK.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Tony Knutson and Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
SOF-ELK related files of interest

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from SOFELK to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate SOFELK events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit SOFELK storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SOF-ELK related files of interest
Author: Tony Knutson and Andrew Rathbun
Version: 1.1
Id: bf220343-d374-4257-835f-b74ee8a47f78
RecreateDirectories: true
Targets:
    -
        Name: EventLogs
        Category: Targets
        Path: EventLogs.tkape
    -
        Name: EvidenceOfExecution
        Category: Targets
        Path: EvidenceOfExecution.tkape
    -
        Name: FileSystem
        Category: Targets
        Path: FileSystem.tkape
    -
        Name: LNKFilesAndJumpLists
        Category: Targets
        Path: LNKFilesAndJumpLists.tkape
    -
        Name: Prefetch
        Category: Targets
        Path: Prefetch.tkape

# Documentation
# https://aboutdfir.com/sof-elk-and-integration-with-kape/
# https://github.com/philhagen/sof-elk/blob/main/doc/kape_support.md
# Use with SOFELK_Parser.mkape
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
