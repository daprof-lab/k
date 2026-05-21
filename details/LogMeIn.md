# 🎯 **LogMeIn Client**
### `File Name: LogMeIn.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Session configurations, activity logs, and system settings for LogMeIn remote access.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from LogMeIn Client to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate LogMeIn Client events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit LogMeIn Client storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: LogMeIn Data
Author: Drew Ervin
Version: 1.0
Id: 488e9de2-ecb6-4b27-88a3-719715147c33
RecreateDirectories: true
Targets:
    -
        Name: LogMeIn ProgramData Logs
        Category: ApplicationLogs
        Path: C:\ProgramData\LogMeIn\Logs\
        Recursive: true
    -
        Name: LogMeIn Application Events
        Category: EventLogs
        Path: ApplicationEvents.tkape
        Comment: "Contains LogMeIn entries, event source: LogMeIn"
    -
        Name: LogMeIn Application Logs
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Local\temp\LogMeInLogs\
        Recursive: true
        Comment: "Contains RemoteAssist (formerly GoToAssist), GoToMeeting, and other GoTo* logs"

# Documentation
# https://support.logmeininc.com/pro/help/how-to-view-logmein-event-log-files-logmein-t-host-preferences-log
# https://www.researchgate.net/publication/313796589_An_exploration_of_artefacts_of_remote_desktop_applications_on_Windows
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
