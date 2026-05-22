# 🎯 **Windows Subsystemfor Android**
### `File Name: WindowsSubsystemforAndroid.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Subsystem for Android (WSA)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Subsystemfor Android to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Subsystemfor Android events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Subsystemfor Android storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Subsystem for Android (WSA)
Author: Andrew Rathbun
Version: 1.0
Id: 0e0b5f71-6e93-444e-8109-7a0c902f8361
RecreateDirectories: true
Targets:
    -
        Name: Diagnostic Logs for WSA
        Category: Windows Subsystem for Android
        Path: C:\Users\%user%\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalState\diagnostics\logcat\
        FileMask: "*.log"
        Comment: "Filenames should be %timestamp%.log"
    -
        Name: App download artifacts (PNG)
        Category: Windows Subsystem for Android
        Path: C:\Users\%user%\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalCache\
        FileMask: "*.png"
        Comment: "Will provide examiners with indicators of which apps were downloaded"
    -
        Name: App download artifacts (ICO)
        Category: Windows Subsystem for Android
        Path: C:\Users\%user%\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalCache\
        FileMask: "*.ico"
        Comment: "Will provide examiners with indicators of which apps were downloaded WHEN since .ico files appear immediately when download of an application completes"
    -
        Name: Appcompatdb.json
        Category: Windows Subsystem for Android
        Path: C:\Users\%user%\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalState\
        FileMask: "appcompatdb.json"
        Comment: "Grabs the appcompatdb.json, unknown exactly what this is but further relevance could be uncovered after more research is conducted"
    -
        Name: userdata.vhdx
        Category: Windows Subsystem for Android
        Path: C:\Users\%user%\AppData\Local\Packages\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\LocalCache\
        FileMask: "userdata.vhdx"
        Comment: "Grabs the user's data which appears to be stored in a VHDX"

# Documentation
# https://blogs.windows.com/windows-insider/2021/10/20/introducing-android-apps-on-windows-11-to-windows-insiders/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
