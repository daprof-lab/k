# 🎯 **Chrome Extensions**
### `File Name: ChromeExtensions.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** piesecurity / Reece394  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracted Chromium browser extension packages, local databases, and synced configs.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Chrome Extensions to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Chrome Extensions events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Chrome Extensions storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Chrome Extension Files
Author: piesecurity, Reece394
Version: 1.1
Id: e748b5e3-e279-4e4d-8083-74293e5b6cde
RecreateDirectories: true
Targets:
    -
        Name: Chrome Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome Extension Files XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\Application Data\Google\Chrome\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome Beta Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome Beta\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome Beta Extension Files XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\Application Data\Google\Chrome Beta\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome Dev Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome Dev\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome Dev Extension Files XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\Application Data\Google\Chrome Dev\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome SxS - Canary Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome SxS\User Data\*\Extensions\
        Recursive: true
    -
        Name: Chrome SxS - Canary Extension Files XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\Application Data\Google\Chrome SxS\User Data\*\Extensions\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
