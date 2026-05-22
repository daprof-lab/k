# 🎯 **Radmin**
### `File Name: Radmin.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mathias Frank  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Radmin Server/Viewer Logs and Chats

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Radmin to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Radmin events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Radmin storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Radmin Server/Viewer Logs and Chats
Author: Mathias Frank
Version: 1.0
Id: 432a2374-2310-461e-ad94-aaf07989aa46
RecreateDirectories: true
Targets:
    -
        Name: Radmin Server 32bit Log
        Category: ApplicationLogs
        Path: C:\Windows\SysWOW64\rserver30\
        FileMask: Radm_log.htm
        Comment: "Contains Application Log entries such as service start and incomming connections."
    -
        Name: Radmin Server 64bit Log
        Category: ApplicationLogs
        Path: C:\Windows\System32\rserver30\
        FileMask: Radm_log.htm
        Comment: "Contains Application Log entries such as service start and incomming connections."
    -
        Name: Radmin Server 32bit Chats
        Category: ApplicationLogs
        Path: C:\Windows\SysWOW64\rserver30\CHATLOGS\*\
        FileMask: '*.htm'
        Comment: "Previous chat logs"
    -
        Name: Radmin Server 64bit Chats
        Category: ApplicationLogs
        Path: C:\Windows\System32\rserver30\CHATLOGS\*\
        FileMask: '*.htm'
        Comment: "Previous chat logs"
    -
        Name: Radmin Viewer Chats
        Category: ApplicationLogs
        Path: C:\Users\%user%\Documents\ChatLogs\*\
        FileMask: '*.htm'
        Comment: "Previous chat logs"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
