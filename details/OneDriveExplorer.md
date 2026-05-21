# ⚙️ **OneDrive Explorer**
### `File Name: OneDriveExplorer.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Brian Maloney  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
Decrypts and parses OneDrive sync databases to map synchronized file structures, deletions, and hashes.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run OneDrive Explorer to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw OneDrive Explorer logs to index file anomalies.
* **Incident Impact Assessment**: Leverage OneDrive Explorer timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'OneDriveExplorer: process OneDrive .dat and .previous.dat files'
Category: FileKnowledge
Author: Brian Maloney
Version: 1.3
Id: 6a2d7872-9eeb-4614-9090-b61a9ada2bba
BinaryUrl: https://github.com/Beercow/OneDriveExplorer/releases/latest
ExportFormat: csv
Processors:
    -
        Executable: OneDriveExplorer.exe
        CommandLine: --LIVE %sourceDirectory% --output-dir %destinationDirectory% --csv
        ExportFormat: csv
    -
        Executable: OneDriveExplorer.exe
        CommandLine: --LIVE %sourceDirectory% --output-dir %destinationDirectory% --html
        ExportFormat: html
    -
        Executable: OneDriveExplorer.exe
        CommandLine: --LIVE %sourceDirectory% --output-dir %destinationDirectory% --json
        ExportFormat: json

# Documentation
# https://github.com/Beercow/OneDriveExplorer
# https://www.sans.org/blog/recreating-onedrive-s-folder-structure-from-usercid-dat/
# As of version v2022.06.17, if you would like to parse ODL logs add --LOGS to the command
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
