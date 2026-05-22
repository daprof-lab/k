# ⚙️ **Mftecmd $MFT Dump Resident Files**
### `File Name: MFTECmd_$MFT_DumpResidentFiles.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd: process $MFT files, then dump resident files within the $MFT

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mftecmd $MFT Dump Resident Files to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mftecmd $MFT Dump Resident Files logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mftecmd $MFT Dump Resident Files timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process $MFT files, then dump resident files within the $MFT'
Category: FileSystem
Author: Andrew Rathbun
Version: 1.0
Id: 4b9ba0a9-1453-438f-94c7-8344bed6ad82
BinaryUrl: https://download.ericzimmermanstools.com/MFTECmd.zip
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory% --dr --ir
        ExportFormat: csv

# Documentation
# https://github.com/EricZimmerman/MFTECmd
# https://binaryforay.blogspot.com/2018/06/introducing-mftecmd.html
# https://aboutdfir.com/toolsandartifacts/windows/mft-explorer-mftecmd/
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# Use this Module to dump all resident files that currently reside within a given $MFT into .\%destinationDirectory%\Resident
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
