# ⚙️ **Reg Hunter Shell**
### `File Name: reg_hunter_shell.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter Shell module to find command shells (cmd.exe, powershell.exe, ...)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Shell to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Shell logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Shell timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter Shell module to find command shells (cmd.exe, powershell.exe, ...)
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: de0ced67-fa0d-4bf0-9022-27b2a2457917
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --shell --outfile %destinationDirectory%\reg_hunter_shell.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
