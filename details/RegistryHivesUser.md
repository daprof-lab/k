# 🎯 **User Registry Hives**
### `File Name: RegistryHivesUser.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman / Mark Hallman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
User-level registry database files (NTUSER.DAT and UsrClass.dat). These store individual user workspace configurations, recent file usage, shellbags, and application habits.

---

## 🔍 **Investigative Use-Cases**
* **User Navigation Tracking (Shellbags)**: Reconstruct a user's navigation through local and network directories, even if the folders have been deleted.
* **Command Execution Profiling (RunMRU)**: Audit commands typed directly into the Run dialog box by a user or script.
* **Recent File Interaction (RecentDocs)**: Identify files recently opened or saved by a specific user profile.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: User Related Registry hives
Author: Eric Zimmerman / Mark Hallman
Version: 1.0
Id: 635fbfd3-4a47-45b5-aae4-0a1bb6545d08
RecreateDirectories: true
Targets:
    -
        Name: NTUSER.DAT registry hive XP
        Category: Registry
        Path: C:\Documents and Settings\%user%\
        FileMask: NTUSER.DAT*
    -
        Name: NTUSER.DAT registry hive
        Category: Registry
        Path: C:\Users\%user%\
        FileMask: NTUSER.DAT*
    -
        Name: NTUSER.DAT registry transaction files
        Category: Registry
        Path: C:\Users\%user%\
        FileMask: NTUSER.DAT.LOG*
    -
        Name: NTUSER.DAT DEFAULT registry hive
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: DEFAULT
    -
        Name: NTUSER.DAT DEFAULT registry hive
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: DEFAULT
    -
        Name: NTUSER.DAT DEFAULT transaction files
        Category: Registry
        Path: C:\Windows\System32\config\
        FileMask: DEFAULT.LOG*
    -
        Name: NTUSER.DAT DEFAULT transaction files
        Category: Registry
        Path: C:\Windows.old\Windows\System32\config\
        FileMask: DEFAULT.LOG*
    -
        Name: UsrClass.dat registry hive
        Category: Registry
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\
        FileMask: UsrClass.dat*
    -
        Name: UsrClass.dat registry transaction files
        Category: Registry
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\
        FileMask: UsrClass.dat.LOG*

# Documentation
# https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download
# https://www.youtube.com/watch?v=OBp6SHgSSZg
# https://www.secjuice.com/windows-forensics-artifacts-2/
# https://www.sans.org/reading-room/whitepapers/forensics/windows-shellbag-forensics-in-depth-34545
# https://cyberforensicator.com/2019/02/03/shellbags-forensics-directory-viewing-preferences/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
