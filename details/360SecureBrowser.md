# 🎯 **360secure Browser**
### `File Name: 360SecureBrowser.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Reece394, Yogesh Khatri  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
360 Secure Browser

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from 360secure Browser to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate 360secure Browser events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit 360secure Browser storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: 360 Secure Browser
Author: Reece394, Yogesh Khatri
Version: 1.1
Id: 243c9a21-3b4a-48b8-9fc7-740f36f2ea37
RecreateDirectories: true
Targets:
    -
        Name: 360 Secure Browser Bookmarks
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: 360Bookmarks*
    -
        Name: 360 Secure Browser Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        Recursive: true
        FileMask: Cookies*
    -
        Name: 360 Secure Browser Current Session
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Current Session
    -
        Name: 360 Secure Browser Current Tabs
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Current Tabs
    -
        Name: 360 Secure Browser Download Metadata
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: DownloadMetadata
    -
        Name: 360 Secure Browser Extension Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Extension Cookies
    -
        Name: 360 Secure Browser Favicons
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Favicons*
    -
        Name: 360 Secure Browser History
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: 360History*
    -
        Name: 360 Secure Browser Last Session
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Last Session
    -
        Name: 360 Secure Browser Last Tabs
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Last Tabs
    -
        Name: 360 Secure Browser Sessions Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\Sessions\
        Recursive: false
    -
        Name: 360 Secure Browser Login Data
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Login Data*
    -
        Name: 360 Secure Browser Media History
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Media History*
    -
        Name: 360 Secure Browser Network Action Predictor
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Network Action Predictor
    -
        Name: 360 Secure Browser Network Persistent State
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        Recursive: true
        FileMask: Network Persistent State
    -
        Name: 360 Secure Browser Preferences
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Preferences
    -
        Name: 360 Secure Browser Secure Preferences
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Secure Preferences
    -
        Name: 360 Secure Browser Quota Manager
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: QuotaManager
    -
        Name: 360 Secure Browser Reporting and NEL
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        Recursive: true
        FileMask: Reporting and NEL
    -
        Name: 360 Secure Browser Shortcuts
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Shortcuts*
    -
        Name: 360 Secure Browser Top Sites
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Top Sites*
    -
        Name: 360 Secure Browser Trust Tokens
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        Recursive: true
        FileMask: Trust Tokens*
    -
        Name: 360 Secure Browser SyncData Database
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\Sync Data
        Recursive: true
    -
        Name: 360 Secure Browser Visited Links
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Visited Links
    -
        Name: 360 Secure Browser Web Data
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\*\
        FileMask: Web Data*
    -
        Name: Windows Protect Folder
        Category: FileSystem
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Protect\*\
        Recursive: true
        Comment: "Required for offline decryption"
    -
        Name: 360 Secure Browser Snapshots Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\360se6\User Data\Snapshots\*\
        Recursive: true
        Comment: "Grabs folder that appears to have snapshots of 360 Secure Browser SQLite DBs organized by version #."

# Documentation
# https://browser.360.cn/
# https://forensafe.com/blogs/360securebrowser.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
