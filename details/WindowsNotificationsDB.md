# 🎯 **Windows Notifications DB**
### `File Name: WindowsNotificationsDB.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Hadar Yudovich  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows 10 Notification DB

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Notifications DB to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Notifications DB events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Notifications DB storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows 10 Notification DB
Author: Hadar Yudovich
Version: 1.0
Id: a5c3308d-8941-43c4-a295-b906a59bc895
RecreateDirectories: true
Targets:
    -
        Name: Windows 10 Notification DB
        Category: Notifications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Notifications\
        FileMask: wpndatabase.db*
    -
        Name: Windows 10 Notification DB
        Category: Notifications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Notifications\
        FileMask: appdb.dat

# Documentation
# https://www.swiftforensics.com/2016/06/prasing-windows-10-notification-database.html
# https://www.hecfblog.com/2018/08/daily-blog-440-windows-10-notifications.html
# https://inc0x0.com/2018/10/windows-10-notification-database/
# https://www.forensafe.com/blogs/win10notifications.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
