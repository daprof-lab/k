# 🎯 **Windows Defender**
### `File Name: WindowsDefender.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Detection logs, scan configurations, quarantined assets metadata, and logs from Microsoft AV.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Defender to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Defender events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Defender storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Defender Data
Author: Drew Ervin
Version: 1.0
Id: 061aa929-292b-4d7f-a4af-a3fe2673a3e5
RecreateDirectories: true
Targets:
    -
        Name: Windows Defender Logs
        Category: Antivirus
        Path: C:\ProgramData\Microsoft\Microsoft AntiMalware\Support\
        Recursive: true
    -
        Name: Windows Defender Event Logs
        Category: EventLogs
        Path: C:\Windows\System32\winevt\Logs\
        FileMask: Microsoft-Windows-Windows Defender*.evtx
    -
        Name: Windows Defender Event Logs
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\Logs\
        FileMask: Microsoft-Windows-Windows Defender*.evtx
    -
        Name: Windows Defender Logs
        Category: Antivirus
        Path: C:\ProgramData\Microsoft\Windows Defender\Support\
        Recursive: true
    -
        Name: Windows Defender Logs
        Category: Antivirus
        Path: C:\Windows\Temp\
        FileMask: MpCmdRun.log
    -
        Name: Windows Defender Logs
        Category: Antivirus
        Path: C:\Windows.old\Windows\Temp\
        FileMask: MpCmdRun.log
    -
        Name: DetectionHistory
        Category: Antivirus
        Path: C:\ProgramData\Microsoft\Windows Defender\Scans\History\Service\DetectionHistory\*\
        Recursive: true
    -
        Name: Windows Defender Quarantine
        Category: Antivirus
        Path: C:\ProgramData\Microsoft\Windows Defender\Quarantine\
        Recursive: true
    -
        Name: Windows Defender Detections.log
        Category: Antivirus
        Path: C:\ProgramData\Microsoft\Windows Defender\Scans\History\Service\
        FileMask: Detections.log

# Documentation
# https://knez.github.io/posts/how-to-extract-quarantine-files-from-windows-defender/
# https://www.crowdstrike.com/blog/how-to-use-microsoft-protection-logging-for-forensic-investigations/
# https://github.com/jklepsercyber/defender-detectionhistory-parser/blob/main/README.md
# https://forensafe.com/blogs/windows_defender.html
# https://www.thedfirspot.com/post/windows-defender-mp-logs-a-story-of-artifacts
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
