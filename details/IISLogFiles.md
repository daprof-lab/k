# 🎯 **IIS Web Server Logs**
### `File Name: IISLogFiles.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Troy Larson  
**Version:** 3.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
HTTP request logs, client user-agents, IP addresses, and response status from IIS instances.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from IIS Web Server Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate IIS Web Server Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit IIS Web Server Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IIS Log Files
Author: Troy Larson
Version: 3.0
Id: 701573f6-0ce1-454d-af41-612713e22af5
RecreateDirectories: true
Targets:
    -
        Name: IIS log files
        Category: Logs
        Path: C:\Windows\System32\LogFiles\W3SVC*\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\Windows.old\Windows\System32\LogFiles\W3SVC*\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\inetpub\logs\LogFiles\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\inetpub\logs\LogFiles\W3SVC*\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\Resources\Directory\*\LogFiles\Web\W3SVC*\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\Windows\system32\LogFiles\HTTPERR\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\inetpub\logs\LogFiles\FTPSVC*\
        FileMask: '*.log'
    -
        Name: IIS log files
        Category: Logs
        Path: C:\inetpub\logs\LogFiles\*\
        Recursive: true
        FileMask: '*.log'

# Documentation
# https://www.sumologic.com/blog/iis-log-files-location/
# http://journeyintoir.blogspot.com/2014/07/ (Section starting with: "In addition to the IIS logs in the W3SVC1 folder, the HTTP.sys error loggingx...")
# https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2003/cc786081(v=ws.10)
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
