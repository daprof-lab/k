# ⚙️ **Sys Internals Ps Info**
### `File Name: SysInternals_PsInfo.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PsInfo is a command-line tool that gathers key information about the local or remote Windows NT/2000 system, including the type of installation, kernel build, registered organization and owner, number of processors and their type, amount of physical memory, the install date of the system, and if its a trial version, the expiration date.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Ps Info to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Ps Info logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Ps Info timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: PsInfo is a command-line tool that gathers key information about the local or remote Windows NT/2000 system, including the type of installation, kernel build, registered organization and owner, number of processors and their type, amount of physical memory, the install date of the system, and if its a trial version, the expiration date.
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: 9e89b787-bc97-4e96-b72e-195a390ede98
BinaryUrl: https://download.sysinternals.com/files/PSTools.zip
ExportFormat: csv
Processors:
    -
        Executable: PsInfo.exe
        CommandLine: -h -s -d -c -accepteula
        ExportFormat: csv
        ExportFile: psinfo.csv

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/psinfo
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
