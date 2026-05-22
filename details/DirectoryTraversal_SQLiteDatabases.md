# 🎯 **Directory Traversal Sqlite Databases**
### `File Name: DirectoryTraversal_SQLiteDatabases.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find files with common SQLite file extensions

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Sqlite Databases to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Sqlite Databases events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Sqlite Databases storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find files with common SQLite file extensions
Author: Andrew Rathbun
Version: 1.0
Id: b5ed4735-9c21-44f0-91a1-1a29f16a9fe5
RecreateDirectories: true
Targets:
    -
        Name: SQLite Files (.db* and .sqlite*)
        Category: Databases
        Path: C:\
        FileMask: regex:*.+\.(db*|sqlite*|)
        Recursive: true
        Comment: Covers all common file extensions for SQLite databases

# Documentation
# https://en.wikipedia.org/wiki/SQLite
# Please note this Target will not grab SQLite databases for Chromium-based browsers as those files usually don't have a file extension, i.e. the filenames are History, Media History, etc, but they are still SQLite databases
# Searching by file header is the only true way to find every SQLite database across an entire drive, but this Target combined with SQLiteDatabases Target will grab most, if not all of the useful databases known to be of forensic value
# Also please note that just because a file has an extension that fits the above does not mean it's a SQLite database. The best way to verify is to throw the file into a SQLite DB Viewer
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
