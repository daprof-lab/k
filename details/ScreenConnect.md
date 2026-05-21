# 🎯 **ScreenConnect Client**
### `File Name: ScreenConnect.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Logs, server configs, and diagnostic metrics from ConnectWise/ScreenConnect agents.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from ScreenConnect Client to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate ScreenConnect Client events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit ScreenConnect Client storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ScreenConnect Data (now known as ConnectWise Control)
Author: Drew Ervin
Version: 1.0
Id: 26c80b79-b3c0-4378-abe8-a5a6c9aebb4f
RecreateDirectories: true
Targets:
    -
        Name: ScreenConnect Session Database
        Category: ApplicationLogs
        Path: C:\Program Files*\ScreenConnect\App_Data\
        FileMask: Session.db
        Comment: "SQLite database with session information"
    -
        Name: ScreenConnect Session Database
        Category: ApplicationLogs
        Path: C:\Program Files*\ScreenConnect\App_Data\
        FileMask: User.xml
        Comment: "Contains each user's last authenticated time"
    -
        Name: ScreenConnect Application Events
        Category: EventLogs
        Path: ApplicationEvents.tkape
        Comment: "Contains ScreenConnect entries, source: ScreenConnect Client"
    -
        Name: ScreenConnect User Config
        Category: ApplicationLogs
        Path: C:\ProgramData\ScreenConnect Client*\
        FileMask: user.config
        Comment: "Contains server domain and IP info"

# Documentation
# https://youtu.be/0qSWfbti4yM
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
