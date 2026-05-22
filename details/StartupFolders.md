# 🎯 **Startup Folders**
### `File Name: StartupFolders.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Jason Ballard  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Startup Folders

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Startup Folders to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Startup Folders events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Startup Folders storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Startup Folders
Author: Jason Ballard
Version: 1.0
Id: 95408ecb-0adb-4a13-8b3d-a36e7f70b6b6
RecreateDirectories: true
Targets:
    -
        Name: User startup folders
        Category: Persistence
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
    -
        Name: System-wide startup folder
        Category: Persistence
        Path: C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp

# Documentation
# https://attack.mitre.org/techniques/T1547/001/
# These programs will be executed under the context of the user and will have the account's associated permissions level.
# This is a fairly common persistence mechanism
# Placing a program or .lnk (shortcut) file in the System-wide startup folder will cause each program to execute when a user logs in, regardless of which user.
# Placing a program or .lnk (shortcut) file in a user startup folder will cause that program to execute when that specific user logs in.
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
