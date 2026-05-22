# 🎯 **Sabnbzd**
### `File Name: SABnbzd.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SABnbzd

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Sabnbzd to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Sabnbzd events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Sabnbzd storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SABnbzd
Author: Andrew Rathbun
Version: 1.0
Id: 315fb563-fe32-4efb-a1b8-1be4d05023ef
RecreateDirectories: true
Targets:
    -
        Name: Usenet Clients - SABnzbd Download Logs
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\sabnzbd\logs\
        FileMask: 'sabnzbd.log'
        Comment: "Locates SABnzbd download log"
    -
        Name: Usenet Clients - SABnzbd History.db
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\sabnzbd\admin\
        FileMask: 'history1.db'
        Comment: "Locates SABnzbd history log"

# Documentation
# C:\Users\%user%\AppData\Local\sabnzbd\logs\sabnzbd.log is where a verbose log file exists.
# C:\Users\%user%\AppData\Local\sabnzbd\admin\history1.db appears to show a history of filenames of NZBs used by the user.
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
