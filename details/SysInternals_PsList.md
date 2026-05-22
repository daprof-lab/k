# ⚙️ **Sys Internals Ps List**
### `File Name: SysInternals_PsList.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Shows statistics for all running processes

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Ps List to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Ps List logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Ps List timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Shows statistics for all running processes
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: fa3aa32a-0091-4650-9485-ad87891b8751
BinaryUrl: https://download.sysinternals.com/files/PSTools.zip
ExportFormat: txt
Processors:
    -
        Executable: pslist.exe
        CommandLine: -x -accepteula
        ExportFormat: txt
        ExportFile: pslist.txt

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/pslist
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
