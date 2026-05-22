# 🎯 **Idrive**
### `File Name: IDrive.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas Burnette  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IDrive Backup Artifacts

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Idrive to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Idrive events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Idrive storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IDrive Backup Artifacts
Author: Thomas Burnette
Version: 1.0
Id: d5f9d7ac-4b34-47ad-beda-123c6f9cf73e
RecreateDirectories: true
Targets:
    -
        Name: IDrive Cleanup Operations
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\Session\Archive Cleanup\
        Recursive: true
        FileMask: "*"
        Comment: "Contains individual log files for each archive cleanup operation"
    -
        Name: IDrive Backup Operations
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\Session\Backup\
        Recursive: true
        FileMask: "*"
        Comment: "Contains individual log files for each backup operation"
    -
        Name: IDrive Delete Operations
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\Session\Delete\
        Recursive: true
        FileMask: "*"
        Comment: "Contains individual log files for each delete operation"
    -
        Name: IDrive Restore Operations
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\Session\Restore\
        FileMask: "*"
        Comment: "Contains individual log files for each restore operation"
    -
        Name: IDrive Backup Summary
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\Session\LOGXML\
        FileMask: "*xml"
        Comment: "Contains summary of each backup session"
    -
        Name: IDrive Tracefile
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\
        FileMask: "Tracefile.txt"
        Comment: "Application log which includes error logs for failed uploads"
    -
        Name: IDrive Mapped Drives
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "IDMappedDrives.txt"
        Comment: "List of mapped drives for backup"
    -
        Name: IDrive Backup Schedule
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "schedule.xml"
        Comment: "Backup schedule configurations"
    -
        Name: IDrive Schedule History
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "Sch_Trace.txt"
        Comment: "History of schedule configurations"
    -
        Name: IDrive Configuration
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "idrive.ini"
        Comment: "List of IDrive configuration options"
    -
        Name: IDrive Local Drives
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "get_Alldrives.txt"
        Comment: "List of all local drives"
    -
        Name: IDrive Exclusion Configurations
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "Exclude*"
        Comment: "Files pertaining to exclusion configurations"
    -
        Name: IDrive User Details
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\
        FileMask: "AutoComp.ini"
        Comment: "IDrive username, Scheduler notification emails, local username"
    -
        Name: IDrive SQL Databse
        Category: Apps
        Path: C:\ProgramData\IDrive\IBCOMMON\*\LDBNEW\*\
        FileMask: "*.ibds"
        Comment: "Sql database of local files that are backed up"

# Documentation
# https://www.idrive.com/
# IDrive provides Online cloud Backup for PCs, Macs, iPhones, Android and other Mobile Devices.
# The most important files are likely to be the log files locatd in C:\ProgramData\IDrive\IBCOMMON\*\Session\Backup\*.
# A new log file is created for each backup session and contains the file name, directory, file size, and time of backup for each file as well as a backup summary.
# The next most important file is likely to be C:\ProgramData\IDrive\IBCOMMON\*\LDBNEW\*\*.ibds, which is a Sqlite database that contains the file name, directory, and file size of files that are backed up from a local drive.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
