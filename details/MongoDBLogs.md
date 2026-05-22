# 🎯 **Mongo Dblogs**
### `File Name: MongoDBLogs.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Eric Capuano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MongoDB Log Files (Windows)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mongo Dblogs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mongo Dblogs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mongo Dblogs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MongoDB Log Files (Windows)
Author: Eric Capuano
Version: 1.0
Id: 2e5c341b-d10a-466d-a40e-abb478212e00
RecreateDirectories: true
Targets:
    -
        Name: MongoDB Logs (Program Files)
        Category: Logs
        Path: C:\Program Files\MongoDB\Server\*\log\
        Recursive: true
        FileMask: "*.log*"
        Comment: "MongoDB log files in default MSI install log directory"
    -
        Name: MongoDB Logs (Program Files - logs folder)
        Category: Logs
        Path: C:\Program Files\MongoDB\Server\*\logs\
        Recursive: true
        FileMask: "*.log*"
        Comment: "MongoDB log files when folder is named 'logs'"
    -
        Name: MongoDB Logs (C:\data\log)
        Category: Logs
        Path: C:\data\log\
        Recursive: true
        FileMask: "*.log*"
        Comment: "Common default MongoDB log directory for manual installations"
    -
        Name: MongoDB Logs (ProgramData)
        Category: Logs
        Path: C:\ProgramData\MongoDB\log\
        Recursive: true
        FileMask: "*.log*"
        Comment: "Log directory for MongoDB Windows service installations"
    -
        Name: MongoDB Logs (Alternate Install)
        Category: Logs
        Path: C:\MongoDB\log\
        Recursive: true
        FileMask: "*.log*"
        Comment: "Common non-default install log directory"

# Documentation
# https://www.mongodb.com/docs/manual/reference/log-messages/
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
