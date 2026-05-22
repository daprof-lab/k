# 🎯 **Heidi SQL**
### `File Name: HeidiSQL.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Hyun Yi @hyuunnn  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
HeidiSQL

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Heidi SQL to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Heidi SQL events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Heidi SQL storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: HeidiSQL
Author: Hyun Yi @hyuunnn
Version: 1.0
Id: aac45152-ac7d-4a5e-9f51-523b45b0d9e6
RecreateDirectories: true
Targets:
    -
        Name: HeidiSQL Backup files (*.sql)
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\HeidiSQL\Backups\
    -
        Name: HeidiSQL (tabs.ini)
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\HeidiSQL\
        FileMask: tabs.ini

# Documentation
# N/A
# C:\Users\%user%\AppData\Roaming\HeidiSQL\Backups\query-tab-2020-12-14_13-09-19-655.sql
# C:\Users\%user%\AppData\Roaming\HeidiSQL\tabs.ini
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
