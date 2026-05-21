# ⚙️ **MFTECmd Parser**
### `File Name: MFTECmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Executes Eric Zimmerman's MFTECmd tool to process raw `$MFT`, `$Boot`, `$LogFile`, and `$J` files into structured, timeline-friendly CSV tables.

---

## 🔍 **Investigative Use-Cases**
* **Bulk MFT Re-indexing**: Extract and index millions of MFT records into CSV tables to analyze directory paths and file extensions.
* **USN Journal Reconstruction**: Timeline all file operations, showing file creation, rename, and deletion events from raw USN change logs.
* **NTFS Operation Mapping**: Analyze $LogFile metadata transactions to isolate deleted file details and short-term disk states.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process all files handled by MFTECmd'
Category: FileSystem
Author: Eric Zimmerman
Version: 1.0
Id: 7ef84a6b-5215-47bb-af2a-2139a3277e25
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/MFTECmd.zip
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: MFTECmd_$Boot.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: MFTECmd_$MFT.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: MFTECmd_$J.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: MFTECmd_$SDS.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://github.com/EricZimmerman/MFTECmd
# https://binaryforay.blogspot.com/2018/06/introducing-mftecmd.html
# https://aboutdfir.com/toolsandartifacts/windows/mft-explorer-mftecmd/
# https://www.youtube.com/watch?v=GhCZfCzn2l0
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
