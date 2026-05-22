# ⚙️ **Sys Internals Ps Tree**
### `File Name: SysInternals_PsTree.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Shows a basic process tree for all running processes

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Ps Tree to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Ps Tree logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Ps Tree timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Shows a basic process tree for all running processes
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: df6c02c1-d4b9-4e84-a4f6-7dd3f67a319d
BinaryUrl: https://download.sysinternals.com/files/PSTools.zip
ExportFormat: txt
Processors:
    -
        Executable: pslist.exe
        CommandLine: -t -accepteula
        ExportFormat: txt
        ExportFile: pstree.txt

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/pslist
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
