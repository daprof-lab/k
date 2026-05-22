# 🎯 **Sugar Sync**
### `File Name: SugarSync.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SugarSync

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Sugar Sync to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Sugar Sync events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Sugar Sync storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SugarSync
Author: Andrew Rathbun
Version: 1.0
Id: 91e7965c-d9ed-440e-93b7-65d7ebdb3584
RecreateDirectories: true
Targets:
    -
        Name: SugarSync Log File
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\SugarSync\
        FileMask: 'sc1.log'
        Comment: "Locates a log file the gives a play-by-play of what the user synced when."
    -
        Name: SugarSync - Shared Folders (Default Location)
        Category: Apps
        Path: C:\Users\%user%\Documents\SugarSync Shared Folders\
        Recursive: true
    -
        Name: SugarSync - My SugarSync (Default Location)
        Category: Apps
        Path: C:\Users\%user%\Documents\My SugarSync\
        Recursive: true

# Documentation
# SugarSync is an online storage service similar to Google Drive, OneDrive, etc. I had never heard of it, but it's one of 4 online storage services listed as an option on Ninite as of October 2020.
# The sc1.log file appears to be the only thing relevant for this application.
# Please note, this is not like OneDrive, Google Drive, etc where there's a dedicated folder where what is stored in SugarSync resides locally on the system. The user can choose folders all around their system to sync to SugarSync as changes are made on their system.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
