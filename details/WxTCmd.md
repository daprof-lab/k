# ⚙️ **WxTCmd Timeline Parser**
### `File Name: WxTCmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs WxTCmd to parse Windows Timeline SQLite databases (ActivitiesCache.db), timelines user application focuses, opened documents, and clipboard logs.

---

## 🔍 **Investigative Use-Cases**
* **User Focused Timeline Building**: Map exact sequences of documents and web pages viewed with active screen focus during the compromise.
* **Clipboard Data Leak Audits**: Recover copied text segments containing passwords, commands, or source code histories.
* **Account Sync Audits**: Audit multi-system sync patterns to check if remote attacker systems synchronized data pools.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'WxTCmd.exe: process Windows Timeline/Activities Cache files'
Category: FileFolderAccess
Author: Mike Cary
Version: 1.0
Id: 47b717ab-9a2f-4eb6-a79f-9f56b2c076c4
BinaryUrl: https://download.ericzimmermanstools.com/WxTCmd.zip
ExportFormat: csv
FileMask: ActivitiesCache.db
Processors:
    -
        Executable: WxTCmd.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory%
        ExportFormat: csv

# Documentation
# https://github.com/EricZimmerman/WxTCmd
# https://binaryforay.blogspot.com/2018/05/introducing-wxtcmd.html
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
