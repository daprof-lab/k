# ⚙️ **Sys Internals Handle**
### `File Name: SysInternals_Handle.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Handle is a utility that displays information about open handles for any process in the system.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Handle to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Handle logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Handle timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Handle is a utility that displays information about open handles for any process in the system.
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: de522157-2cde-46ff-b1b0-d2201fba6554
BinaryUrl: https://download.sysinternals.com/files/Handle.zip
ExportFormat: txt
Processors:
    -
        Executable: handle.exe
        CommandLine: -a -u -accepteula
        ExportFormat: txt
        ExportFile: handles.txt

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/handle
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
