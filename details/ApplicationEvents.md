# 🎯 **Application Events**
### `File Name: ApplicationEvents.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Application Event Log

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Application Events to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Application Events events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Application Events storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Application Event Log
Author: Drew Ervin
Version: 1.0
Id: 2da16dbf-ea47-448e-a00f-fc442c3109ba
RecreateDirectories: true
Targets:
    -
        Name: Application Event Log XP
        Category: EventLogs
        Path: C:\Windows\System32\config\
        FileMask: AppEvent.evt
    -
        Name: Application Event Log XP
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: AppEvent.evt
    -
        Name: Application Event Log Win7+
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: application.evtx
    -
        Name: Application Event Log Win7+
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: application.evtx

# Documentation
# https://countuponsecurity.com/2015/11/23/digital-forensics-supertimeline-event-logs-part-i/
# https://www.jaiminton.com/cheatsheet/DFIR/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
