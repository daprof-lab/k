# 🎯 **Windows Timeline Database**
### `File Name: WindowsTimeline.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Lee Whitfield / Thomas DIOT  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
SQLite database containing user activity logs (ActivitiesCache.db). It records opened files, clipboard copies, application focus histories, and connected external devices.

---

## 🔍 **Investigative Use-Cases**
* **User Focused Timeline Mapping**: Determine which document, web page, or application had active user focus at any specific timestamp.
* **Clipboard History Auditing**: Recover copied text segments, passwords, or shell scripts stored in the Windows Clipboard.
* **Cross-Device Sync Analysis**: Map a user's movement across synchronized workstations connected to the same Microsoft account.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ActivitiesCache.db collector
Author: Lee Whitfield, Thomas DIOT (Qazeer)
Version: 1.1
Id: 8315040f-c9a4-455a-b02c-96372583f436
RecreateDirectories: true
Targets:
    -
        Name: ActivitiesCache.db
        Category: FileFolderAccess
        Path: C:\Users\%user%\AppData\Local\ConnectedDevicesPlatform\
        Recursive: true
        FileMask: ActivitiesCache.db*

# Documentation
# https://www.group-ib.com/blog/windows10_timeline_for_forensics
# https://kacos2000.github.io/WindowsTimeline/WindowsTimeline.pdf
# https://medium.com/@soji256/list-of-windows-10-timeline-analysis-articles-c61595b49e0d
# https://www.cellebrite.com/en/blog/exploring-the-windows-activity-timeline-part-1-the-high-points/
# https://www.andreafortuna.org/2019/10/03/some-forensic-thoughts-about-windows-10-timeline/
# https://salt4n6.com/2018/05/03/windows-10-timeline-forensic-artefacts/
# https://cyberforensicator.com/2018/05/08/wxtcmd-windows-10-timeline-parser/
# https://www.forensafe.com/blogs/wintimeline.html
# There is a SQLECmd map for the ActivitiesCache.db database: https://github.com/EricZimmerman/SQLECmd/blob/master/SQLMap/Maps/Windows_ActivitiesCache.smap
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
