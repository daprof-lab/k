# 🎯 **Event Logs RDP Eae7bdd6 93f1 4e06 Ae0f 2c64c9f1c7c6**
### `File Name: EventLogs-RDP_eae7bdd6-93f1-4e06-ae0f-2c64c9f1c7c6.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Mark Hallman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collect Win7+ RDP related Event logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Event Logs RDP Eae7bdd6 93f1 4e06 Ae0f 2c64c9f1c7c6 to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Event Logs RDP Eae7bdd6 93f1 4e06 Ae0f 2c64c9f1c7c6 events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Event Logs RDP Eae7bdd6 93f1 4e06 Ae0f 2c64c9f1c7c6 storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Collect Win7+ RDP related Event logs
Author: Mark Hallman
Version: 1.0
Id: 2e79fc64-816c-439a-8b7f-93dd59bf2711
RecreateDirectories: true
Targets:
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: System.evtx
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: System.evtx
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: Security.evtx
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: Security.evtx
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows\System32\winevt\Logs\Microsoft-Windows-TerminalServices-LocalSessionManager%4Operational.evtx
        FileMask: Microsoft-Windows-TerminalServices-LocalSessionManager%4Operational.evtx
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows\System32\winevt\Logs\
        FileMask: Microsoft-Windows-TerminalServices-RemoteConnectionManager%4Operational.evtx

# Documentation
# https://medium.com/@lucideus/introduction-to-event-log-analysis-part-1-windows-forensics-manual-2018-b936a1a35d8a
# https://medium.com/@lucideus/event-log-analysis-part-2-windows-forensics-manual-2018-75710851e323
# https://www.digitalforensics.com/blog/forensic-analysis-of-windows-event-logs-windows-files-activities-audit/
# https://youtu.be/Xw536W7kbDQ
# https://www.youtube.com/watch?v=myzG11BP3Sk
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
