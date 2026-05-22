# ⚙️ **Sys Internals Sig Check**
### `File Name: SysInternals_SigCheck.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** troyla@microsoft.com  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Sigcheck all files in a volume, with hashes, entropy, and internal metadata

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Sig Check to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Sig Check logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Sig Check timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Sigcheck all files in a volume, with hashes, entropy, and internal metadata
Category: FileMetadata
Author: troyla@microsoft.com
Version: 1.0
Id: f93bd081-55cd-4c13-9a7f-280a0caeebf8
BinaryUrl: https://download.sysinternals.com/files/Sigcheck.zip
ExportFormat: csv
Processors:
    -
        Executable: sigcheck64.exe
        CommandLine: -a -c -h -s -accepteula -nobanner %sourceDirectory%
        ExportFormat: csv
        ExportFile: sigcheck.csv

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/sigcheck
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
