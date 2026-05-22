# ⚙️ **Mftecmd $MFT Process Mftslack**
### `File Name: MFTECmd_$MFT_ProcessMFTSlack.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd: process $MFT files with FILE slack recovery

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mftecmd $MFT Process Mftslack to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mftecmd $MFT Process Mftslack logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mftecmd $MFT Process Mftslack timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process $MFT files with FILE slack recovery'
Category: FileSystem
Author: Andrew Rathbun
Version: 1.0
Id: 69553b37-e8d9-4ae9-b325-bc0dd2808a71
BinaryUrl: https://download.ericzimmermanstools.com/MFTECmd.zip
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --csv %destinationDirectory% --rs
        ExportFormat: csv
        ExportFile: MFTFileSlack.txt
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --json %destinationDirectory% --rs
        ExportFormat: json
        ExportFile: MFTFileSlack.txt

# Documentation
# https://github.com/EricZimmerman/MFTECmd
# https://docs.microsoft.com/en-us/windows/win32/fileio/master-file-table
# https://binaryforay.blogspot.com/2018/06/introducing-mftecmd.html
# https://aboutdfir.com/toolsandartifacts/windows/mft-explorer-mftecmd/
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# Every FILE record is checked when using this Module. The output will be exported into the FileSystem output folder via the data displayed in the console that is exported to a text file
# Debug messages in KAPE is always recommend for troubleshooting purposes and more verbose messaging that can prove to be helpful in Modules like this one (and many others)
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
