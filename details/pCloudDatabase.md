# 🎯 **P Cloud Database**
### `File Name: pCloudDatabase.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Josh Hickman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
pCloud Database

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from P Cloud Database to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate P Cloud Database events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit P Cloud Database storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: pCloud Database
Author: Josh Hickman
Version: 1.0
Id: dc6750d8-ee91-45d4-9f53-fa3f8513ada3
RecreateDirectories: true
Targets:
    -
        Name: pCloud Database
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\pCloud\
        FileMask: '*.db'
        Recursive: false
        Comment: "Database contains all files sync'd with pCloud account."
    -
        Name: pCloud Database WAL File
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\pCloud\
        FileMask: '*.db-wal'
        Recursive: false
        Comment: "Write-Ahead Log for pCloud database file."
    -
        Name: pCloud Database Shared Memory File
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\pCloud\
        FileMask: '*.db-shm'
        Recursive: false
        Comment: "Shared Memory for the pCloud database file."

# Documentation
# https://cyberforensicator.com/2018/05/05/cloud-forensics-pcloud-drive/
# https://www.sciencedirect.com/science/article/pii/B9780128053034000137
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
