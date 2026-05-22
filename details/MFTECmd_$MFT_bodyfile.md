# ⚙️ **Mftecmd $MFT Bodyfile**
### `File Name: MFTECmd_$MFT_bodyfile.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Angry-Bender  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MFTECmd: process $MFT files and output a bodyfile for mactime / tsk

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mftecmd $MFT Bodyfile to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mftecmd $MFT Bodyfile logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mftecmd $MFT Bodyfile timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'MFTECmd: process $MFT files and output a bodyfile for mactime / tsk'
Category: FileSysten
Author: Angry-Bender
Version: 1.0
Id: 6d2af4e9-fc28-4b4f-ab23-5a21b4e7d802
BinaryUrl: https://download.ericzimmermanstools.com/net9/MFTECmd.zip
ExportFormat: txt
FileMask: $MFT
Processors:
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --body %destinationDirectory% --bdl c
        ExportFormat: txt

# Documentation
# https://github.com/EricZimmerman/MFTECmd
# https://docs.microsoft.com/en-us/windows/win32/fileio/master-file-table
# https://binaryforay.blogspot.com/2018/06/introducing-mftecmd.html
# https://aboutdfir.com/toolsandartifacts/windows/mft-explorer-mftecmd/
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# https://www.thedigitalforensics.com/incident-response/filesystem-based-timeline
# https://frsecure.com/blog/file-system-forensic-analysis/
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
