# 🎯 **Global Browser Caches**
### `File Name: BrowserCache.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Bjorn Vanhaeren, Reece394  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Unified browser cache tables and web assets directories for Chrome, Edge, and Firefox.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Global Browser Caches to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Global Browser Caches events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Global Browser Caches storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Browser Caches
Author: Bjorn Vanhaeren, Reece394
Version: 1.2
Id: bbb89525-6b8d-41f6-acdf-a4f513455703
RecreateDirectories: true
Targets:
    -
        Name: Chrome Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome\User Data\*\Cache\
        Recursive: true
    -
        Name: Chrome Beta Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome Beta\User Data\*\Cache\
        Recursive: true
    -
        Name: Chrome Dev Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome Dev\User Data\*\Cache\
        Recursive: true
    -
        Name: Chrome SxS - Canary Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Google\Chrome SxS\User Data\*\Cache\
        Recursive: true
    -
        Name: Chromium Edge Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge\User Data\*\Cache\
        Recursive: true
    -
        Name: Chromium Edge Beta Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge Beta\User Data\*\Cache\
        Recursive: true
    -
        Name: Chromium Edge Dev Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge Dev\User Data\*\Cache\
        Recursive: true
    -
        Name: Chromium Edge SxS - Canary Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge SxS\User Data\*\Cache\
        Recursive: true
    -
        Name: Chromium Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Chromium\User Data\*\Cache\
        Recursive: true
    -
        Name: Firefox Cache Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Mozilla\Firefox\Profiles\*\
        Recursive: true
    -
        Name: IE 9/10 Cache
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Temporary Internet Files\
        Recursive: true
    -
        Name: IE Index.dat temp internet files
        Category: Communications
        Path: C:\Documents and Settings\%user%\Local Settings\Temporary Internet Files\Content.IE5\
        FileMask: index.dat
    -
        Name: IE 11 Cache
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\INetCache\
        Recursive: true
    -
        Name: Edge WebcacheV01.dat
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\WebCache\
    -
        Name: Brave Cache Folder
        Category: Communications
        Path: C:\Users\%users%\AppData\Local\BraveSoftware\Brave-Browser\User Data\Default\Cache\Cache_Data
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
