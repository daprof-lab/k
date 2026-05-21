# ⚙️ **SrumECmd SRUM Parser**
### `File Name: SrumECmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs SrumECmd to parse srudb.dat databases, detailing historic application network uploads, downloads, battery usage, and CPU times.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Upload Discovery**: Analyze byte transmission logs per executable to locate high-volume data exfiltrations.
* **Deleted Executable Network History**: Verify if deleted binaries or unrecognized scripts made external network connections over a 30-day window.
* **System Active Hours Mapping**: Reconstruct system usage cycles based on application energy consumption and background push states.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'SrumECmd: SRUM Parser'
Category: SRUMDatabase
Author: Andrew Rathbun
Version: 1.1
Id: a0fac3f5-ee99-4973-b3ea-4cffc87da48d
BinaryUrl: https://download.ericzimmermanstools.com/SrumECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: SrumECmd.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory%
        ExportFormat: csv
        ExportFile: SrumECmdConsoleLog.txt

# Documentation
# https://leanpub.com/eztoolsmanuals
# https://github.com/EricZimmerman/Srum/blob/master/README.md will show you how to repair the SRUDB.dat prior to successfully parsing.
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
