# ⚙️ **Sys Internals Ps File**
### `File Name: SysInternals_PsFile.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PsFile is a command-line utility that shows a list of files on a system that are opened remotely, and it also allows you to close opened files either by name or by a file identifier.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Ps File to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Ps File logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Ps File timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: PsFile is a command-line utility that shows a list of files on a system that are opened remotely, and it also allows you to close opened files either by name or by a file identifier.
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: 79cca355-160d-4a61-951d-e295a8c0d8bb
BinaryUrl: https://download.sysinternals.com/files/PSTools.zip
ExportFormat: txt
Processors:
    -
        Executable: psfile.exe
        CommandLine: -accepteula
        ExportFormat: txt
        ExportFile: psfile.txt

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/psfile
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
