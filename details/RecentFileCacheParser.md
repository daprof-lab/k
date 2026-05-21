# ⚙️ **RecentFileCache Parser**
### `File Name: RecentFileCacheParser.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parses legacy RecentFileCache.bcf files to recover application execution histories from older versions of Windows.

---

## 🔍 **Investigative Use-Cases**
* **Legacy Forensic Analysis**: Audit process execution pathways on legacy Windows 7/Server 2008 configurations.
* **Staged Backdoor Timelining**: Verify execution timelines of temporary administrative utilities run during compromise.
* **Reconstruct Executable Paths**: Extract lists of file names and system paths for executed software.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RecentFileCacheParser: extract file names from RecentFilecache.bcf'
Category: ProgramExecution
Author: Eric Zimmerman
Version: 1.0
Id: 32fa31cc-8be6-4a1d-917a-97fbdff552ef
BinaryUrl: https://download.ericzimmermanstools.com/RecentFileCacheParser.zip
ExportFormat: csv
FileMask: RecentFileCache.bcf
Processors:
    -
        Executable: RecentFileCacheParser.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory%
        ExportFormat: csv
    -
        Executable: RecentFileCacheParser.exe
        CommandLine: -f %sourceFile% --json %destinationDirectory%
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/RecentFileCacheParser
# https://www.youtube.com/watch?v=ZKlyu-HOvxY
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
