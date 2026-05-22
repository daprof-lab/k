# ⚙️ **Sys Internals Ps Service**
### `File Name: SysInternals_PsService.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Display the configured services (both running and stopped) on the local system.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Ps Service to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Ps Service logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Ps Service timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Display the configured services (both running and stopped) on the local system.
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: b5af1e38-2a78-4538-8430-83b8a60e02c4
BinaryUrl: https://download.sysinternals.com/files/PSTools.zip
ExportFormat: txt
Processors:
    -
        Executable: PsService.exe
        CommandLine: -accepteula
        ExportFormat: txt
        ExportFile: PsService.txt

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/psservice
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
