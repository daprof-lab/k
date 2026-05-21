# ⚙️ **RBCmd Recycle Bin Parser**
### `File Name: RBCmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs RBCmd to parse Windows Recycle Bin metadata files, resolving raw deleted files to original paths, file sizes, and deletion times.

---

## 🔍 **Investigative Use-Cases**
* **Anti-Forensics Audit**: Match deleted executable metadata against timelines of network breach alerts to identify payload cleanup.
* **Deleted Files Restoration**: Extract and cross-reference deleted documents to rebuild lists of stolen or trashed records.
* **User File Management Timeline**: Analyze user habits by chronologically sorting file deletions in user Recycle directories.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RBCmd: process recycle bin artifacts'
Category: FileDeletion
Author: Eric Zimmerman
Version: 1.0
Id: 7ef84a6b-5115-45bb-aa5b-2249a3237e75
BinaryUrl: https://download.ericzimmermanstools.com/RBCmd.zip
ExportFormat: csv
Processors:
    -
        Executable: RBCmd.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory% -q
        ExportFormat: csv

# Documentation
# https://github.com/EricZimmerman/RBCmd
# https://thinkdfir.com/2018/11/23/quick-post-notes-on-the-win10-recycle-bin/
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
