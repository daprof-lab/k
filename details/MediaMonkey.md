# 🎯 **Media Monkey**
### `File Name: MediaMonkey.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MediaMonkey

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Media Monkey to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Media Monkey events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Media Monkey storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MediaMonkey
Author: Andrew Rathbun
Version: 1.0
Id: d37bb0d2-6870-4159-8823-e0943fc42ae2
RecreateDirectories: true
Targets:
    -
        Name: MediaMonkey - Media SQLite Database
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\MediaMonkey
        FileMask: 'MM.DB'
        Comment: "Locates SQLite DB that contains a complete enumeration of the user's media collection within MediaMonkey"
    -
        Name: MediaMonkey - MediaMonkey.ini
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\MediaMonkey
        FileMask: 'MediaMonkey.ini'
        Comment: "Locates .ini file which contains information about the user's MediaMonkey application instance"

# Documentation
# https://www.mediamonkey.com/support/knowledge-base/mediamonkey-install-config/modifying-the-mediamonkey-db-and-ini-files/
# MediaMonkey is a popular media organizing, tagging, and playing application for Windows
# MM.DB contains information about any files added to a user's MediaMonkey library, including music and video files
# MediaMonkey.ini will contain file paths pointing to where a user stores media that's being viewed within MediaMonkey
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
