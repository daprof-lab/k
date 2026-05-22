# 🎯 **Yandex**
### `File Name: Yandex.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Sebastian Søgaard  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Yandex Artifacts

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Yandex to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Yandex events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Yandex storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Yandex Artifacts
Author: Sebastian Søgaard
Version: 1.0
Id: 32399a9d-d891-49cc-9919-fa45cbe63683
RecreateDirectories: true
Targets:
    -
        Name: Yandex Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        Recursive: true
        FileMask: Cookies*
    -
        Name: Yandex Network Persistent State
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        Recursive: true
        FileMask: Network Persistent State
    -
        Name: Yandex Favicons
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Favicons*
    -
        Name: Yandex History
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: History*
    -
        Name: Yandex Sessions Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\Sessions\
        Recursive: false
    -
        Name: Yandex Login Data
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Ya Passman Data*
    -
        Name: Yandex Network Action Predictor
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Network Action Predictor
    -
        Name: Yandex Preferences
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Preferences
    -
        Name: Yandex Top Sites
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Top Sites*
    -
        Name: Yandex Bookmarks
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Bookmarks*
    -
        Name: Yandex Visited Links
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Visited Links
    -
        Name: Yandex Web Data
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Web Data*
    -
        Name: Yandex Autofill data
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Ya Autofill Data*
    -
        Name: Yandex Passman logs
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Passman Logs*
    -
        Name: Yandex Shortcuts
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Yandex\YandexBrowser\User Data\*\
        FileMask: Shortcuts*

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
