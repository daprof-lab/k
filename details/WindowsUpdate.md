# 🎯 **Windows Update**
### `File Name: WindowsUpdate.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Rick van Dreunen  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Update Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Update to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Update events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Update storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Update Logs
Author: Rick van Dreunen
Version: 1.0
Id: 38d1263b-0d8d-42e1-a1c1-d933a854a474
RecreateDirectories: true
Targets:
    -
        Name: Windows Update Session Orchestrator logs
        Category: EventLogs
        Path: C:\ProgramData\USOShared\Logs\System\
        FileMask: '*.etl'
        Recursive: true
    -
        Name: Windows Update logs
        Category: EventLogs
        Path: C:\Windows\Logs\WindowsUpdate\
        FileMask: 'WindowsUpdate*.etl'
        Recursive: true
    -
        Name: Windows Component-Based Servicing logs
        Category: EventLogs
        Path: C:\Windows\Logs\CBS\
        FileMask: 'CBS*.log'
        Recursive: true
    -
        Name: Windows Update History
        Category: EventLogs
        Path: C:\Windows\SoftwareDistribution\DataStore
        Recursive: true

# Documentation
# https://learn.microsoft.com/en-us/windows/deployment/update/windows-update-logs
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
