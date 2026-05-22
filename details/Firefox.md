# 🎯 **Mozilla Firefox**
### `File Name: Firefox.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Eric Zimmerman and Andrew Rathbun  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Profile folders, history databases (places.sqlite), cookies, extensions, and bookmarks.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mozilla Firefox to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mozilla Firefox events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mozilla Firefox storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Firefox
Author: Eric Zimmerman and Andrew Rathbun
Version: 1.2
Id: 28801734-b95a-47e7-b84f-4ebd0c104862
RecreateDirectories: true
Targets:
    -
        Name: Addons
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: addons.sqlite*
    -
        Name: Bookmarks
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\weave\
        FileMask: bookmarks.sqlite*
    -
        Name: Bookmarks
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\bookmarkbackups
        Recursive: true
    -
        Name: Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: cookies.sqlite*
    -
        Name: Cookies
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: firefox_cookies.sqlite*
    -
        Name: Downloads
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: downloads.sqlite*
    -
        Name: Extensions
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: extensions.json
    -
        Name: Favicons
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: favicons.sqlite*
    -
        Name: Form history
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: formhistory.sqlite*
    -
        Name: Permissions
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: permissions.sqlite*
    -
        Name: Places
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: places.sqlite*
    -
        Name: Protections
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: protections.sqlite*
    -
        Name: Search
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: search.sqlite*
    -
        Name: Signons
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: signons.sqlite*
    -
        Name: Storage Sync
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: storage-sync.sqlite*
    -
        Name: Webappstore
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: webappstore.sqlite*
    -
        Name: Password
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: key*.db
    -
        Name: Password
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: signon*.*
    -
        Name: Password
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: logins.json
    -
        Name: Preferences
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: prefs.js
    -
        Name: Sessionstore
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\
        FileMask: sessionstore*
    -
        Name: Sessionstore Folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Mozilla\Firefox\Profiles\*\sessionstore-backups
        Recursive: true
    -
        Name: Places XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: places.sqlite*
    -
        Name: Downloads XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: downloads.sqlite*
    -
        Name: Form history XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: formhistory.sqlite*
    -
        Name: Cookies XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: cookies.sqlite*
    -
        Name: Signons XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: signons.sqlite*
    -
        Name: Webappstore XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: webappstore.sqlite*
    -
        Name: Favicons XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: favicons.sqlite*
    -
        Name: Addons XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: addons.sqlite*
    -
        Name: Search XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: search.sqlite*
    -
        Name: Password XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: key*.db
    -
        Name: Password XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: signon*.*
    -
        Name: Password XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: logins.json
    -
        Name: Sessionstore XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Mozilla\Firefox\Profiles\*\
        FileMask: sessionstore*

# Documentation
# https://www.4n6k.com/2017/11/forensics-quickie-identifying-clear.html
# https://www.digitalforensics.com/blog/an-overview-of-web-browser-forensics/
# https://www.foxtonforensics.com/browser-history-examiner/firefox-history-location
# https://www.forensafe.com/blogs/firefox.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
