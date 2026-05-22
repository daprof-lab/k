# 🎯 **VS Code Workspace**
### `File Name: VisualStudioCode.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Sebastian Søgaard, ogmini  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Editor history, settings, recently opened workspaces, and extensions history for VS Code.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VS Code Workspace to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VS Code Workspace events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VS Code Workspace storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Visual Studio Code artifacts
Author: Sebastian Søgaard, ogmini
Version: 2.0
Id: f90fe4ce-b349-4010-8d41-3b7b8273e5fe
RecreateDirectories: true
Targets:
    -
        Name: VSCode Opened Files
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\User\History\*\
        Recursive: true
        Comment: "Grabs the files in the VSCode history. These are files the user has opened with VSCode"
    -
        Name: VSCode Workspaces
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\User\globalStorage\
        FileMask: storage.json*
        Comment: "Grabs the file containing information about the user's workspaces"
    -
        Name: VSCode User extensions
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\CachedExtensions\
        FileMask: user*
        Comment: "Grabs the files relating to the user's installed extensions"
    -
        Name: VSCode User settings
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\User\
        FileMask: settings.json*
        Comment: "Grabs the file containing the settings the user has set."
    -
        Name: VSCode User Preferences
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\
        FileMask: preferences*
        Comment: "Grabs the file containing the preferences the user has set."
    -
        Name: VSCode Network Cookies
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\Network\
        FileMask: Cookies*
        Comment: "Grabs the cookie files. Same format as Chromium Cookies"
    -
        Name: VSCode Network Persistent State
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\Network\
        FileMask: Network Persistent State*
        Comment: "Grabs the Network Persistent State file. Same format as in  Chromium"
    -
        Name: VSCode Logs
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\logs\
        Recursive: true
        Comment: "Grabs the VSCode logs. Further analysis is needed to determine which logs are junk, and which can be vital."
    -
        Name: VSCode File Backups
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Code\Backups\*\
        Recursive: true
        Comment: "Grabs the Backups for unsaved changes."

# Documentation
# https://ogmini.github.io/2025/02/22/Investigating-Visual-Studio-Code-Part-3.html - Specific writeup on the Backups and History folders and files.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
