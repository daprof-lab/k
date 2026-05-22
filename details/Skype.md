# 🎯 **Skype Desktop**
### `File Name: Skype.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Eric Zimmerman, Matt Dawson  
**Version:** 4.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Historical databases of messages, contacts list, calls, and shared transfer files.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Skype Desktop to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Skype Desktop events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Skype Desktop storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Skype
Author: Eric Zimmerman, Matt Dawson
Version: 4.0
Id: d7b0b49c-16bb-4b32-9f57-2d918acaebbc
RecreateDirectories: true
Targets:
    -
        Name: main.db (App <v12)
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.SkypeApp_*\LocalState\*\
        FileMask: main.db
    -
        Name: skype.db (App +v12)
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.SkypeApp_*\LocalState\*\
        FileMask: skype.db
    -
        Name: main.db XP
        Category: Communications
        Path: C:\Documents and Settings\%user%\Application Data\Skype\*\
        FileMask: main.db
    -
        Name: main.db Win7+
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Skype\*\
        FileMask: main.db
    -
        Name: s4l-[username].db (App +v8)
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.SkypeApp_*\LocalState\
        FileMask: s4l-*.db
    -
        Name: leveldb (Skype for Desktop +v8)
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Skype for Desktop\IndexedDB\*.leveldb\
        Recursive: true
    -
        Name: Skype for Destkop v8+ Chromium Cache
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\Microsoft\Skype for Desktop\Cache\
        Recursive: true
        Comment: Can be viewed with Nirsoft's ChromeCacheView

# Documentation
# https://bebinary4n6.blogspot.com/2019/07/analysis-of-skype-windows-10-app.html
# https://bebinary4n6.blogspot.com/2019/07/skype-from-old-one-to-newest-one.html
# https://blog.elcomsoft.com/2019/12/extracting-skype-histories-and-deleted-files-metadata-from-microsoft-account/
# https://bebinary4n6.blogspot.com/2019/07/analysis-skype-app-for-windows-metro.html
# https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/microsoft-teams-and-skype-logging-privacy-issue/
# https://www.forensafe.com/blogs/skype.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
