# 🎯 **Icon Cache DB**
### `File Name: IconCacheDB.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Herbert Bärschneider @SEC Consult  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
IconCache.db files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Icon Cache DB to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Icon Cache DB events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Icon Cache DB storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IconCache.db files
Author: Herbert Bärschneider @SEC Consult
Version: 1.0
Id: 4e447ad0-4fda-44f6-9f82-1ae9ac47a8d4
RecreateDirectories: true
Targets:
    -
        Name: Windows IconCache DB
        Category: IconCache
        Path: C:\Users\%user%\AppData\Local\
        FileMask: IconCache.db

# Documentation
# https://www.sciencedirect.com/science/article/abs/pii/S1742287614000607
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
