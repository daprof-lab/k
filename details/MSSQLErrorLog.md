# 🎯 **Mssqlerror Log**
### `File Name: MSSQLErrorLog.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Troy Larson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MS SQL ErrorLogs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mssqlerror Log to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mssqlerror Log events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mssqlerror Log storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MS SQL ErrorLogs
Author: Troy Larson
Version: 1.0
Id: cb789cbf-bf4a-4491-b6d9-9e2d002bd85e
RecreateDirectories: true
Targets:
    -
        Name: MS SQL Errorlog
        Category: SQL Exploitation
        Path: C:\Program Files\Microsoft SQL Server\*\MSSQL\LOG\
        FileMask: ERRORLOG
    -
        Name: MS SQL Errorlogs
        Category: SQL Exploitation
        Path: C:\Program Files\Microsoft SQL Server\*\MSSQL\LOG\
        FileMask: ERRORLOG.*

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
