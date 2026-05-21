# ⚙️ **AmcacheParser**
### `File Name: AmcacheParser.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs AmcacheParser to parse Amcache.hve hives, extracting executable execution paths, hashes, compiler times, and installation statuses.

---

## 🔍 **Investigative Use-Cases**
* **Hash Extraction for Threat Hunting**: Extract SHA-1 file hashes of all historical binaries to run automated queries against threat feeds.
* **Malicious Staged File Discovery**: Scan execution pathways of binaries located in remote temp folders or local application data paths.
* **Compiler Timestamp Analysis**: Locate timestomping attempts by comparing actual compiler stamps against metadata creation times.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'AmcacheParser: extract program execution information'
Category: ProgramExecution
Author: Eric Zimmerman
Version: 1.1
Id: 4190c518-524f-4623-8038-a014784c018c
BinaryUrl: https://download.ericzimmermanstools.com/AmcacheParser.zip
ExportFormat: csv
FileMask: Amcache.hve
Processors:
    -
        Executable: AmcacheParser.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory% -i --mp
        ExportFormat: csv

# Documentation
# https://github.com/EricZimmerman/AmcacheParser
# https://binaryforay.blogspot.com/2015/07/amcacheparser-reducing-noise-finding.html
# https://www.youtube.com/watch?v=ZKlyu-HOvxY
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
