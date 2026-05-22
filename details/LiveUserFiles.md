# 🎯 **Live User Files**
### `File Name: LiveUserFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mark Hallman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Live User Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Live User Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Live User Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Live User Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Live User Files
Author: Mark Hallman
Version: 1.0
Id: 2a5cb2e6-20e0-495b-9b6d-8728ac210584
RecreateDirectories: true
Targets:
    -
        Name: User Files - Desktop
        Category: LiveUserFiles
        Path: C:\Users\%user%\Desktop\
        Recursive: true
    -
        Name: User Files - Documents
        Category: LiveUserFiles
        Path: C:\Users\%user%\Documents\
        Recursive: true
    -
        Name: User Files - Downloads
        Category: LiveUserFiles
        Path: C:\Users\%user%\Downloads\
        Recursive: true
    -
        Name: User Files - Dropbox
        Category: LiveUserFiles
        Path: C:\Users\%user%\Dropbox*\
        Recursive: true
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
