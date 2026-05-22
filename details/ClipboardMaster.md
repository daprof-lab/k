# 🎯 **Clipboard Master**
### `File Name: ClipboardMaster.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ClipboardMaster

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Clipboard Master to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Clipboard Master events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Clipboard Master storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ClipboardMaster
Author: Andrew Rathbun
Version: 1.0
Id: 43decd24-2ab6-40cc-9b78-23c7f720906b
RecreateDirectories: true
Targets:
    -
        Name: ClipboardMaster - Clipboard History - Text
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Jumping Bytes\ClipboardMaster\
        FileMask: 'Clipboard.clm4'
        Comment: "Locates the user’s clipboard history (text) for ClipboardMaster"
    -
        Name: ClipboardMaster - Clipboard History - Images
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Jumping Bytes\ClipboardMaster\pics\
        Recursive: true
        Comment: "Locates the user’s clipboard history (images) for ClipboardMaster"
    -
        Name: ClipboardMaster - Clipboard History - Backups
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Jumping Bytes\ClipboardMaster\
        FileMask: 'Clipboard.clm4.ba*'
        Comment: "Locates the user’s clipboard history (backups) for ClipboardMaster"

# Documentation
# Clipboard Master is a universal multi-clipboard for text, images, files, etc for Windows XP+.
# Clipboard.clm4 can be viewed in any text editor. It appears to store in plaintext the user’s clipboard history.
# Clipboard.clm.bak appears to be a 1:1 backup of Clipboard.clm4.
# There appeared to be multiple files with the naming convention ofClipboard.clm4.ba# where # iterated from 2 upward. These were also plaintext readable in any text editor.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
