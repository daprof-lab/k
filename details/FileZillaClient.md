# 🎯 **FileZilla Client Sessions**
### `File Name: FileZillaClient.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Dennis Reneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
XML and SQLite configurations containing recent servers list, transfer logs, and credentials database.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from FileZilla Client Sessions to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate FileZilla Client Sessions events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit FileZilla Client Sessions storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: FileZilla XML and SQLite Log Files
Author: Dennis Reneau
Version: 1.0
Id: f7eaa0d5-0b15-4578-b411-ac4226e13a7f
RecreateDirectories: true
Targets:
    -
        Name: FileZilla XML Log Files
        Category: Logs
        Path: C:\Users\%user%\AppData\Roaming\FileZilla\
        FileMask: '*.xml*'
    -
        Name: FileZilla SQLite3 Log Files
        Category: Logs
        Path: C:\Users\%user%\AppData\Roaming\FileZilla\
        FileMask: '*.sqlite3*'

# Documentation
# https://www.sans.org/reading-room/whitepapers/forensics/evidence-data-exfiltration-containerised-applications-virtual-private-servers-38555
# https://wiki.filezilla-project.org/Logs
# https://www.hecfblog.com/2013/09/daily-blog-93-filezilla-artifacts.html
# https://forensafe.com/blogs/filezilla.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
