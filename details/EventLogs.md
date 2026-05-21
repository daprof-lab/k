# 🎯 **Windows Event Logs**
### `File Name: EventLogs.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System-wide EVTX log files containing core security audits, application logs, and system events.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Event Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Event Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Event Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Event logs
Author: Eric Zimmerman
Version: 1.0
Id: d95784d9-bd1c-472b-aeef-de5d9ecc7aaa
RecreateDirectories: true
Targets:
    -
        Name: Event logs XP
        Category: EventLogs
        Path: C:\Windows\System32\config\
        FileMask: '*.evt'
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows\System32\winevt\logs\
        FileMask: '*.evtx'
    -
        Name: Event logs Win7+
        Category: EventLogs
        Path: C:\Windows.old\Windows\System32\winevt\logs\
        FileMask: '*.evtx'

# Documentation
# https://www.youtube.com/watch?v=qjeA1a5n0LQ
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
