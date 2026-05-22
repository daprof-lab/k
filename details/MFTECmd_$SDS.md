# ⚙️ **Mftecmd $SDS**
### `File Name: MFTECmd_$SDS.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd: process $SDS files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mftecmd $SDS to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mftecmd $SDS logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mftecmd $SDS timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process $SDS files'
Category: FileSystem
Author: Eric Zimmerman
Version: 1.0
Id: 7ef84a6b-5215-46bb-af2a-3339a4247e41
BinaryUrl: https://download.ericzimmermanstools.com/MFTECmd.zip
ExportFormat: csv
FileMask: $Secure_$SDS
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
# https://binaryforay.blogspot.com/2018/06/introducing-mftecmd.html
# https://aboutdfir.com/toolsandartifacts/windows/mft-explorer-mftecmd/
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
