# ⚙️ **Mftecmd $MFT**
### `File Name: MFTECmd_$MFT.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd: process $MFT files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mftecmd $MFT to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mftecmd $MFT logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mftecmd $MFT timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process $MFT files'
Category: FileSystem
Author: Eric Zimmerman
Version: 1.0
Id: 7ef84a6b-5215-46bb-af2a-3339a3227e25
BinaryUrl: https://download.ericzimmermanstools.com/MFTECmd.zip
ExportFormat: csv
FileMask: $MFT
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
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
