# ⚙️ **AppCompatCacheParser (Shimcache)**
### `File Name: AppCompatCacheParser.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs AppCompatCacheParser to extract execution records from the SYSTEM registry hive, locating file paths and execution status.

---

## 🔍 **Investigative Use-Cases**
* **Autostart Binary Auditing**: Reconstruct a timeline of system process execution, finding binaries that ran prior to the incident.
* **System Integrity Assessment**: Detect process paths of hacktools or staging payloads run from system volumes.
* **Application Execution Chronology**: Timeline registry execution indicators to map lateral movement patterns during threat hunting.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'AppCompatCacheParser: extract AppCompatCache (shimcache) information'
Category: ProgramExecution
Author: Eric Zimmerman
Version: 1.1
Id: e5e0ffa8-fe3e-4196-ac5a-d21cbeb879c2
BinaryUrl: https://download.ericzimmermanstools.com/AppCompatCacheParser.zip
ExportFormat: csv
FileMask: SYSTEM
Processors:
    -
        Executable: AppCompatCacheParser.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory%
        ExportFormat: csv

# Documentation
# https://github.com/EricZimmerman/AppCompatCacheParser
# https://binaryforay.blogspot.com/2015/05/introducing-appcompatcacheparser.html
# https://kzclip.com/video/ZKlyu-HOvxY/windows-application-compatibility-forensics.html
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
