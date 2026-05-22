# 🎯 **Chat GPT**
### `File Name: ChatGPT.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ogmini  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
A Target to collect files related to ChatGPT Desktop

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Chat GPT to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Chat GPT events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Chat GPT storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: A Target to collect files related to ChatGPT Desktop
Author: ogmini
Version: 1.0
Id: 7e0d5a5f-66d1-46aa-9f1c-6cbfe9fe35ac
RecreateDirectories: true
Targets:
    -
        Name: LevelDB
        Category: Database
        Path: C:\Users\%user%\AppData\Local\Packages\OpenAI.ChatGPT-Desktop_2p2nqsd0c76g0\LocalCache\Roaming\ChatGPT\Local Storage\leveldb
        FileMask: "*"
        Comment: "LevelDB Database"
    -
        Name: IndexedDB
        Category: Database
        Path: C:\Users\%user%\AppData\Local\Packages\OpenAI.ChatGPT-Desktop_2p2nqsd0c76g0\LocalCache\Roaming\ChatGPT\IndexedDB\https_chatgpt.com_0.indexeddb.leveldb
        FileMask: "*"
        Comment: "IndexedDB Database"
    -
        Name: ChromeCache
        Category: Cache
        Path: C:\Users\%user%\AppData\Local\Packages\OpenAI.ChatGPT-Desktop_2p2nqsd0c76g0\LocalCache\Roaming\ChatGPT\Cache
        Recursive: true
        FileMask: "*"
        Comment: "Chrome Cache"
    -
        Name: Helium Registry Hives
        Category: Application Registry
        Path: C:\Users\%user%\AppData\Local\Packages\OpenAI.ChatGPT-Desktop_2p2nqsd0c76g0\SystemAppData\Helium
        FileMask: "*.dat"
        Comment: "Retrieves User.dat and UserClasses.dat which are Application Registries"
    -
        Name: ChatGPT Settings File
        Category: Application Registry
        Path: C:\Users\%user%\AppData\Local\Packages\OpenAI.ChatGPT-Desktop_2p2nqsd0c76g0\Settings
        FileMask: "settings.dat"
        Comment: "Retrieves settings.dat which is an Application Registry"

# Documentation
# https://ogmini.github.io/2025/01/20/David-Cowen-Sunday-Funday-ChatGPT.html
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
