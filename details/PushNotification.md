# 🎯 **Push Notification**
### `File Name: PushNotification.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Zawadi Done  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Push Notification Service

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Push Notification to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Push Notification events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Push Notification storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Push Notification Service
Author: Zawadi Done
Version: 1.0
Id: 49545136-dddd-4255-a5b5-c977bb72fded
RecreateDirectories: true
Targets:
    -
        Name: WNS
        Category: WNS
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Notifications\
        FileMask: appdb.dat
    -
        Name: WNS
        Category: WNS
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Notifications\
        FileMask: wpndatabase.db

# Documentation
# https://forensafe.com/blogs/winnotifications.html
# https://learn.microsoft.com/en-us/windows/apps/design/shell/tiles-and-notifications/windows-push-notification-services--wns--overview
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
