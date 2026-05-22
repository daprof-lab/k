# 🎯 **Chrome File System**
### `File Name: ChromeFileSystem.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Chad Tilbury, Reece394  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Chrome HTML5 File System Contents

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Chrome File System to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Chrome File System events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Chrome File System storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Chrome HTML5 File System Contents
Author: Chad Tilbury, Reece394
Version: 1.1
Id: a135eb84-5407-4590-a3e8-02564ebc5fa9
RecreateDirectories: true
Targets:
    -
        Name: Chrome HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome\User Data\*\File System\
        Recursive: true
    -
        Name: Chrome Beta HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome Beta\User Data\*\File System\
        Recursive: true
    -
        Name: Chrome Dev HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome Dev\User Data\*\File System\
        Recursive: true
    -
        Name: Chrome SxS - Canary HTML5 File System Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome SxS\User Data\*\File System\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
