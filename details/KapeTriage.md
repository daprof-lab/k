# 🎯 **KapeTriage Package**
### `File Name: KapeTriage.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Scott Downie  
**Version:** 4.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Comprehensive triage collector gathering File System, Registry, Event Logs, Prefetch, SRUM, and Web Browser history.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from KapeTriage Package to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate KapeTriage Package events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit KapeTriage Package storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: KapeTriage collects most of the files needed for a DFIR Investigation. This Target pulls evidence from File System files, Registry Hives, Event Logs, Scheduled Tasks, Evidence of Execution, SRUM data, SUM data, Cloud metadata, WER, WBEM, Web Browser data (IE/Edge, Chrome, Mozilla history), LNK Files, JumpLists, Notepad unsaved sessions (Win11), 3rd party remote access software logs, 3rd party antivirus software logs, Windows 10/11 Timeline database, and $I Recycle Bin files.
Author: Scott Downie
Version: 4.2
Id: 5e275faa-7bc7-4477-a141-042df174f8bd
RecreateDirectories: true
Targets:
    -
        Name: Antivirus
        Category: Targets
        Path: Antivirus.tkape
    -
        Name: CloudStorage_Metadata
        Category: Targets
        Path: CloudStorage_Metadata.tkape
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
        Name: Notepad
        Category: Targets
        Path: Notepad.tkape
    -
        Name: PowerShellConsole
        Category: Targets
        Path: PowerShellConsole.tkape
    -
        Name: RecycleBin_InfoFiles
        Category: Targets
        Path: RecycleBin_InfoFiles.tkape
    -
        Name: RegistryHives
        Category: Targets
        Path: RegistryHives.tkape
    -
        Name: RemoteAccess
        Category: Targets
        Path: RemoteAdmin.tkape
    -
        Name: ScheduledTasks
        Category: Targets
        Path: ScheduledTasks.tkape
    -
        Name: SRUM
        Category: Targets
        Path: SRUM.tkape
    -
        Name: SUM
        Category: Targets
        Path: SUM.tkape
    -
        Name: WER
        Category: Targets
        Path: WER.tkape
    -
        Name: WBEM
        Category: Targets
        Path: WBEM.tkape
    -
        Name: WebBrowsers
        Category: Targets
        Path: WebBrowsers.tkape
    -
        Name: WindowsTimeline
        Category: Targets
        Path: WindowsTimeline.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
