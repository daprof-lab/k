# 🎯 **Acronis True Image**
### `File Name: AcronisTrueImage.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Acronis True Image

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Acronis True Image to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Acronis True Image events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Acronis True Image storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Acronis True Image
Author: Andrew Rathbun
Version: 1.0
Id: 4f984e18-81fb-4520-9a01-69bf77a0f459
RecreateDirectories: true
Targets:
    -
        Name: Acronis True Image - Logs
        Category: Apps
        Path: C:\ProgramData\Acronis\TrueImageHome\Logs\ti_demon\
        Comment: "Copies out all log files"
    -
        Name: Acronis True Image - Database Files
        Category: Apps
        Path: C:\ProgramData\Acronis\TrueImageHome\Database
        FileMask: archives.db*
        Comment: "Copies out the Database folder which appears to have important information"
    -
        Name: Acronis True Image - Scripts Folder
        Category: Apps
        Path: C:\ProgramData\Acronis\TrueImageHome\Scripts\
        Comment: "Copies out all scripts files"

# Documentation
# http://sersc.org/journals/index.php/IJAST/article/download/17649/8916/
# https://core.ac.uk/download/pdf/214330118.pdf
# Acronis True Image can be used to create full, incremental, and differential backups of any disk/volume on a user's system.
# .\Acronis\TrueImageHome\Logs\ti_demon\ will contain logs that are prepended with ti_demon_ followed by what appears to be either a GUID or gibberish followed by a YYYY-MM-DD-HH-MM-SS timestamp prior to the .log file extension.
# Every time a backup process is started, a log file is created following this naming convention.
# .\Acronis\TrueImageHome\Database\ had a .opt file that I was able to view in a text editor that showed the source and destination for the backup job I created in my testing. It was nested under the "backup_archive_operation_options" with each being on a line that started with "volume_location".
# The Database folder target should get you the files I saw on my system that were relevant (Archives.db, Archives.db-shm, Archives.db-wal, Archives.db000000001h.opt).
# .\Acronis\TrueImageHome\Scripts\ contained .tib.tis files that were viewable in a text editor that appeared to have the contents of a batch script for running the backup I created in my testing.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
