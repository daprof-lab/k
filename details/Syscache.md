# 🎯 **Syscache**
### `File Name: Syscache.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
syscache.hve

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Syscache to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Syscache events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Syscache storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: syscache.hve
Author: Phill Moore
Version: 1.0
Id: d4665b13-9953-4cf0-bdc4-6fcb7a37842f
RecreateDirectories: true
Targets:
    -
        Name: Syscache
        Category: Program Execution
        Path: C:\System Volume Information\
        FileMask: 'Syscache.hve'
    -
        Name: Syscache transaction files
        Category: Program Execution
        Path: C:\System Volume Information\
        FileMask: 'Syscache.hve.LOG*'

# Documentation
# https://dfir.ru/2018/12/02/the-cit-database-and-the-syscache-hive/
# https://www.hecfblog.com/2018/12/daily-blog-579-meaning-of-syscachehve.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
