# 🎯 **Program Execution**
### `File Name: ProgramExecution.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Max Zabuty  
**Version:** 1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Program Execution Triage Collection

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Program Execution to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Program Execution events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Program Execution storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Program Execution Triage Collection
Author: Max Zabuty
Version: 1
Id: c67f2cfe-0664-41d7-9536-daf3be778e84
RecreateDirectories: true
Targets:
    -
        Name: Amcache
        Category: ApplicationCompatibility
        Path: Amcache.tkape
    -
        Name: AppCompatPCA
        Category: ApplicationCompatibility
        Path: AppCompatPCA.tkape
    -
        Name: Prefetch
        Category: Prefetch
        Path: Prefetch.tkape
    -
        Name: RecentFileCache
        Category: ApplicationCompatibility
        Path: RecentFileCache.tkape
    -
        Name: Syscache
        Category: Syscache
        Path: Syscache.tkape
    -
        Name: PowerShellTranscripts
        Category: PowerShellTranscripts
        Path: PowerShellTranscripts.tkape
    -
        Name: PowerShellConsole
        Category: PowerShellConsole
        Path: PowerShellConsole.tkape
    -
        Name: WBEM
        Category: WBEM
        Path: WBEM.tkape
    -
        Name: WER
        Category: WER
        Path: WER.tkape
    -
        Name: WindowsTimeline
        Category: WindowsTimeline
        Path: WindowsTimeline.tkape
    -
        Name: JumpLists
        Category: JumpLists
        Path: JumpLists.tkape
    -
        Name: .NET CLR UsageLogs
        Category: .NET CLR UsageLogs
        Path: NETCLRUsageLogs.tkape

# Documentation
# Collecting different artifacts related to program execution on the host
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
