# 🎯 **TeamViewer Logs**
### `File Name: TeamViewerLogs.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Hadar Yudovich / Sam Smoker  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Connection history logs, remote ID configurations, and session diagnostic tables for TeamViewer.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from TeamViewer Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate TeamViewer Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit TeamViewer Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: TeamViewer Logs
Author: Hadar Yudovich, Sam Smoker
Version: 2.0
Id: 6f2cd531-1f4b-4f0b-aa96-2426621b0a14
RecreateDirectories: true
Targets:
    -
        Name: TeamViewer Connection Logs
        Category: Communications
        Path: C:\Program Files*\TeamViewer\
        FileMask: 'connections*.txt'
        Comment: "Includes connections_incoming.txt and connections.txt"
    -
        Name: TeamViewer Application Logs
        Category: ApplicationLogs
        Path: C:\Program Files*\TeamViewer\
        FileMask: 'TeamViewer*_Logfile*'
        Comment: "Includes TeamViewer<version>_Logfile.log and TeamViewer<version>_Logfile_OLD.log"
    -
        Name: TeamViewer Application User Logs
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Roaming\TeamViewer\
        FileMask: 'TeamViewer*_Logfile*'
        Comment: "Alternate location for TeamViewer<version>_Logfile.log"
    -
        Name: TeamViewer Configuration Files
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Roaming\TeamViewer\MRU\RemoteSupport\
        Recursive: true
        Comment: "Includes miscellaneous config files"

# Documentation
# https://www.champlain.edu/Documents/LCDI/archive/Team-Viewer-Forensics.pdf
# https://svch0st.medium.com/writeup-magnet-user-summit-dfir-ctf-2019-activity-79cf149c04d7
# https://www.systoolsgroup.com/forensics/teamviewer/
# https://athenaforensics.co.uk/teamviewer-forensics/
# https://medium.com/mii-cybersec/digital-forensic-artifact-of-teamviewer-application-cfd6290dc0a7
# https://www.forensafe.com/blogs/teamviewer.html
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
