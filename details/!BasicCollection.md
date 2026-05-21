# 🎯 **Basic Triage Collection**
### `File Name: !BasicCollection.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Light triage target collecting the minimum files required to identify compromised states.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Basic Triage Collection to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Basic Triage Collection events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Basic Triage Collection storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Basic Collection
Author: Phill Moore
Version: 1.1
Id: 83b99299-2d84-4844-af25-c727d3440b19
RecreateDirectories: true
Targets:
    -
        Name: Event Logs
        Category: EventLogs
        Path: EventLogs.tkape
    -
        Name: Evidence of Execution
        Category: EvidenceOfExecution
        Path: EvidenceOfExecution.tkape
    -
        Name: File System
        Category: FileSystem
        Path: FileSystem.tkape
    -
        Name: LNKFilesAndJumpLists
        Category: File Access
        Path: LNKFilesAndJumpLists.tkape
    -
        Name: PowerShellConsole
        Category: EvidenceOfExecution
        Path: PowerShellConsole.tkape
    -
        Name: RecycleBin InfoFiles
        Category: FileDeletion
        Path: RecycleBin_InfoFiles.tkape
    -
        Name: RegistryHives
        Category: Registry Hives
        Path: RegistryHives.tkape
    -
        Name: ScheduledTasks
        Category: ScheduledTasks
        Path: ScheduledTasks.tkape
    -
        Name: SRUM
        Category: SRUM
        Path: SRUM.tkape
    -
        Name: ThumbCache
        Category: Thumbcache
        Path: Thumbcache.tkape
    -
        Name: USBDevicesLogs
        Category: USB
        Path: USBDevicesLogs.tkape
    -
        Name: WindowsIndexSearch
        Category: Search
        Path: WindowsIndexSearch.tkape
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
