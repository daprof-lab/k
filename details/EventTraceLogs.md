# 🎯 **Event Trace Logs**
### `File Name: EventTraceLogs.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mark Hallman  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Event Trace Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Event Trace Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Event Trace Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Event Trace Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Event Trace Logs
Author: Mark Hallman
Version: 1.1
Id: af494526-9e44-4548-9d29-f088eafa6f3d
RecreateDirectories: true
Targets:
    -
        Name: WDI Trace Logs 1
        Category: EventTraceLogs
        Path: C:\Windows\System32\WDI\LogFiles\
        FileMask: '*.etl*'
    -
        Name: WDI Trace Logs 1
        Category: EventTraceLogs
        Path: C:\Windows.old\Windows\System32\WDI\LogFiles\
        FileMask: '*.etl*'
    -
        Name: WDI Trace Logs 2
        Category: EventTraceLogs
        Path: C:\Windows\System32\WDI\{*\
        Recursive: true
    -
        Name: WDI Trace Logs 2
        Category: EventTraceLogs
        Path: C:\Windows.old\Windows\System32\WDI\{*\
        Recursive: true
    -
        Name: WMI Trace Logs
        Category: EventTraceLogs
        Path: C:\Windows\System32\LogFiles\WMI\
        Recursive: true
    -
        Name: WMI Trace Logs
        Category: EventTraceLogs
        Path: C:\Windows.old\Windows\System32\LogFiles\WMI\
        Recursive: true
    -
        Name: SleepStudy Trace Logs
        Category: EventTraceLogs
        Path: C:\Windows\System32\SleepStudy\
        Recursive: true
    -
        Name: SleepStudy Trace Logs
        Category: EventTraceLogs
        Path: C:\Windows.old\Windows\System32\SleepStudy\
        Recursive: true
    -
        Name: Energy-NTKL Trace Logs
        Category: EventTraceLogs
        Path: C:\ProgramData\Microsoft\Windows\PowerEfficiency Diagnostics\
        FileMask: energy-ntkl.etl
    -
        Name: Delivery Optimization Trace Logs
        Category: EventTraceLogs
        Path: C:\Windows\ServiceProfiles\NetworkService\AppData\Local\Microsoft\Windows\DeliveryOptimization\Logs\
        FileMask: '*.etl*'

# Documentation
# https://www.youtube.com/watch?v=TUR-L9AtzQE
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
