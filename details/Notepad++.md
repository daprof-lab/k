# 🎯 **Notepad++ Backups**
### `File Name: Notepad++.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Banaanhangwagen and Matt Dawson  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Unsaved draft buffers, active session backups, and history profiles from Notepad++.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Notepad++ Backups to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Notepad++ Backups events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Notepad++ Backups storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Notepad++ Backups, recently searched/replaced terms and recently opened documents
Author: Banaanhangwagen and Matt Dawson
Version: 2.0
Id: dc6c1009-2d0a-4ead-99f0-d1f3a5380751
RecreateDirectories: true
Targets:
    -
        Name: Notepad++ Unsaved Edits
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Roaming\Notepad++\backup\
        Recursive: true
        Comment: "Locates non-saved Notepad++ files and copies them."
    -
        Name: Notepad++ Config
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Roaming\Notepad++\
        FileMask: "config.xml"
        Comment: "Retrieves config.xml which contains recently searched terms, replaced terms and recently opened documents"
    -
        Name: Notepad++ Session
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Roaming\Notepad++\
        FileMask: "session.xml"
        Comment: "Retrieves session.xml which contains session date"

# Documentation
# https://krknsec.com/2020/04/18/miscellaneous-windows-10-forensic-artifacts
# https://forensafe.com/blogs/windows_notepad++.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
