# 🎯 **Edge File System**
### `File Name: EdgeFileSystem.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Chad Tilbury, Reece394  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Edge HTML5 File System Contents

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Edge File System to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Edge File System events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Edge File System storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Edge HTML5 File System Contents
Author: Chad Tilbury, Reece394
Version: 1.0
Id: 1f8b52a8-0501-43ce-ab26-0a28d53be763
RecreateDirectories: true
Targets:
    -
        Name: Edge HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge\User Data\*\File System\
        Recursive: true
    -
        Name: Edge Beta HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge Beta\User Data\*\File System\
        Recursive: true
    -
        Name: Edge Dev HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge Dev\User Data\*\File System\
        Recursive: true
    -
        Name: Edge SxS - Canary HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge SxS\User Data\*\File System\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
