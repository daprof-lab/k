# 🎯 **Notion**
### `File Name: Notion.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas Burnette  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Notion Note-Taking App

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Notion to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Notion events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Notion storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Notion Note-Taking App
Author: Thomas Burnette
Version: 1.0
Id: 95afe81f-6301-4a7f-996b-c69443e7c2d9
RecreateDirectories: true
Targets:
    -
        Name: Notion Local Storage
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Notion
        FileMask: 'notion.db'
        Comment: "Local storage file containing all pages, databases, users, etc."
    -
        Name: Notion Custom Dictionary
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Notion\Partitions\notion
        FileMask: 'Custom Dictionary.txt'

# Documentation
# https://www.notion.so/
# Notion is a freemium productivity and note-taking app. It includes organizational tools such as task management, project tracking, to-do lists, and bookmarking.
# When using the Notion app for Windows, Notion stores all pages, users, databases, etc. in a SQLite database, notion.db.
# This includes creation and modification timestamps for all entries.
# Additionally, Notion stores the user's Custom Dictionary in a text file.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
