# 🎯 **Combined Logs Package**
### `File Name: CombinedLogs.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Mike Cary / Mark Hallman  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Event Logs, BITS logs, firewall diaries, and PowerShell history transcripts in one click.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Combined Logs Package to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Combined Logs Package events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Combined Logs Package storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collect Event logs, Trace logs, Windows Firewall, PowerShell console logs, and .NET CLR UsageLogs
Author: Mike Cary, Mark Hallman added the USBDevicelogs target, Thomas DIOT (Qazeer) added the .NET CLR UsageLogs and PowerShell Transcripts target
Version: 1.3
Id: d4fdd600-15b1-4b78-bc77-88e724861d8d
RecreateDirectories: true
Targets:
    -
        Name: Windows Event Logs
        Category: EventLogs
        Path: EventLogs.tkape
    -
        Name: Event Trace Logs
        Category: EventTraceLogs
        Path: EventTraceLogs.tkape
    -
        Name: PowerShell Console Log
        Category: PowerShellConsoleLog
        Path: PowerShellConsole.tkape
    -
        Name: PowerShell Transcripts
        Category: PowerShellTranscripts
        Path: PowerShellTranscripts.tkape
    -
        Name: Windows Firewall Log
        Category: WindowsFirewallLogs
        Path: WindowsFirewall.tkape
    -
        Name: USBDevicesLogs
        Category: USB
        Path: USBDevicesLogs.tkape
    -
        Name: .NET CLR UsageLogs
        Category: .NET CLR UsageLogs
        Path: NETCLRUsageLogs.tkape

# Documentation
# v1.1 - Added the USBDevicelogs target
# v1.2 - Added the .NET CLR UsageLogs target
# v1.3 - Added the PowerShell Transcripts target
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
