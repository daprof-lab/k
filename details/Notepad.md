# 🎯 **Notepad Tab State**
### `File Name: Notepad.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun / ogmini  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers active unsaved tabs and text sessions from modern Windows 11 Notepad instances.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Notepad Tab State to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Notepad Tab State events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Notepad Tab State storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: A Target to collect files that are currently open in Notepad (Windows 11+)
Author: Andrew Rathbun, ogmini
Version: 2.0
Id: 53e3b402-e53e-4841-bba0-56e98c53cf5b
RecreateDirectories: true
Targets:
    -
        Name: Notepad Session Files
        Category: Windows Notepad
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.WindowsNotepad_8wekyb3d8bbwe\LocalState\TabState
        FileMask: "*.bin"
        Comment: "Contains .bin files which consist of the files opened in each tab in Windows Notepad"
    -
        Name: Notepad Window State Files
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.WindowsNotepad_8wekyb3d8bbwe\LocalState\WindowState\
        FileMask: "*.bin"
        Comment: "Contains .bin files tracking the state of the Notepad Window"
    -
        Name: Notepad Settings File
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.WindowsNotepad_8wekyb3d8bbwe\Settings\
        FileMask: "settings.dat"
        Comment: "Retrieves settings.dat which is an Application Registry"
    -
        Name: Notepad Registry Hives
        Category: Text Editor
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.WindowsNotepad_8wekyb3d8bbwe\SystemAppData\Helium
        FileMask: "*.dat"
        Comment: "Retrieves User.dat and UserClasses.dat. User.dat contains MRU entries. UserClasses.dat contains Shell Bags."

# Documentation
# https://github.com/ogmini/Notepad-State-Library
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
