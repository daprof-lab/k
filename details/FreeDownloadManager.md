# 🎯 **Free Download Manager**
### `File Name: FreeDownloadManager.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Free Download Manager

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Free Download Manager to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Free Download Manager events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Free Download Manager storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Free Download Manager
Author: Matt Dawson
Version: 1.0
Id: 328c98bc-f5f8-4aff-93c1-53fbf02f5ec7
RecreateDirectories: true
Targets:
    -
        Name: FDM Database
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Free Download Manager\
        Recursive: true
        FileMask: "fdm.sqlite"
        Comment: "fdm.sqlite shows Torrents, downloads, folder history, auth credentials and more. Will also pull fdm.sqlite in db_backup/"
    -
        Name: FDM Backup Info
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Free Download Manager\backup\
        FileMask: "backup.info"
        Comment: "Backup info file - can change backup name from userdata.zip, so could give indication of file name"
    -
        Name: FDM Database (userdata.zip)
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Free Download Manager\backup\
        FileMask: "userdata.zip"
        Comment: "fdm.sqlite can also appear in the backup folder in a compressed userdata.zip file"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
