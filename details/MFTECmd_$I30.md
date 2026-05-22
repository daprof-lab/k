# ⚙️ **Mftecmd $I30**
### `File Name: MFTECmd_$I30.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd: process $INDX/$I30 files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mftecmd $I30 to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mftecmd $I30 logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mftecmd $I30 timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process $INDX/$I30 files'
Category: FileSystem
Author: Phill Moore
Version: 1.0
Id: eccde70f-7828-4a3d-b2dd-0d534516df93
BinaryUrl: https://download.ericzimmermanstools.com/MFTECmd.zip
ExportFormat: csv
FileMask: $I30|INDX
Processors:
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory%
        ExportFormat: csv
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --json %destinationDirectory%
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/MFTECmd
# https://docs.microsoft.com/en-us/windows/win32/fileio/master-file-table
# https://binaryforay.blogspot.com/2018/06/introducing-mftecmd.html
# https://aboutdfir.com/toolsandartifacts/windows/mft-explorer-mftecmd/
# https://thinkdfir.com/2023/01/13/timestamps-in-indx-entries/
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
