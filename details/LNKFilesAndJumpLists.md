# 🎯 **LNK Files & Jump Lists**
### `File Name: LNKFilesAndJumpLists.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman, Andrew Rathbun, Yogesh Khatri  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows shortcut files (.lnk) and taskbar Jump Lists (.automaticDestinations-ms, .customDestinations-ms). These document user file openings and system navigation.

---

## 🔍 **Investigative Use-Cases**
* **Recent Document Verification**: Identify paths, volume serial numbers, and MAC addresses of directories where opened documents originated.
* **External Device Insertion Tracking**: Prove that a document on an external USB flash drive was opened, by examining LNK file parameters.
* **Application Interaction History**: Analyze taskbar Jump Lists to reveal application pin histories and frequent document listings.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: LNK Files and jump lists
Author: Eric Zimmerman, Andrew Rathbun, Yogesh Khatri
Version: 1.3
Id: 2e354bdc-e418-438e-8439-c21c83c64e90
RecreateDirectories: true
Targets:
    -
        Name: LNK Files from Recent
        Category: LNKFiles
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\Recent\
        Recursive: true
        Comment: Also includes automatic and custom jumplist directories
    -
        Name: LNK Files from Microsoft Office Recent
        Category: LNKFiles
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Office\Recent\
        Recursive: true
    -
        Name: Start Menu LNK Files
        Category: LNKFiles
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs
        FileMask: '*.LNK'
    -
        Name: LNK Files from Recent (XP)
        Category: LNKFiles
        Path: C:\Documents and Settings\%user%\Recent\
        Recursive: true
    -
        Name: Desktop LNK Files XP
        Category: LNKFiles
        Path: C:\Documents and Settings\%user%\Desktop\
        FileMask: '*.LNK'
    -
        Name: Desktop LNK Files
        Category: LNKFiles
        Path: C:\Users\%user%\Desktop\
        FileMask: '*.LNK'
    -
        Name: Restore point LNK Files XP
        Category: LNKFiles
        Path: C:\System Volume Information\_restore*\RP*\
        FileMask: '*.LNK'
    -
        Name: LNK Files from C:\ProgramData
        Category: LNKFiles
        Path: C:\ProgramData\Microsoft\Windows\Start Menu\Programs\
        FileMask: '*.LNK'

# Documentation
# https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download
# https://www.youtube.com/watch?v=g1zYCvzhBS4
# https://belkasoft.com/forensic-analysis-of-lnk-files
# http://windowsir.blogspot.com/2017/05/use-of-lnk-filesagain.html
# https://dfir.pubpub.org/pub/wfuxlu9v
# https://www.forensafe.com/blogs/jumplist.html
# https://www.forensafe.com/blogs/lnkfile.html
# https://www.thedfirspot.com/post/a-lnk-to-the-past-utilizing-lnk-files-for-your-investigations
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
