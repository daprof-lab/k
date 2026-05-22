# 🎯 **Viber**
### `File Name: Viber.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Matt Dawson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ViberPC Messaging App

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Viber to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Viber events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Viber storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ViberPC Messaging App
Author: Matt Dawson
Version: 1.0
Id: 61e74d50-5e97-4bc8-a78b-c2fb393d2f9f
RecreateDirectories: true
Targets:
    -
        Name: Viber Config Database
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\ViberPC\
        FileMask: "config.db"
        Comment: "Configuration file for Viber"
    -
        Name: Viber Users Data Database
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\ViberPC\*\
        FileMask: "viber.db"
        Comment: "Viber data for that user, containing Calls, Chat Messages, Contacts and more"
    -
        Name: Viber Users Avatars Cache
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\ViberPC\*\Avatars
        Comment: "Cache of the Avatars for other Viber users"
    -
        Name: Viber Users Backgrounds Cache
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\ViberPC\*\Backgrounds
        Comment: "Store of the backgrounds"
    -
        Name: Viber Users Thumbnails Cache
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\ViberPC\*\Thumbnails
        Comment: "Cache of the thumbnails for uploaded/downloaded images"

# Documentation
# https://www.alexbilz.com/post/2021-01-29-forensic-artifacts-viber-desktop/
# https://www.digitalforensics.com/blog/forensic-analysis-instant-messengers-desktop-applications/
# https://www.forensafe.com/blogs/viber.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
