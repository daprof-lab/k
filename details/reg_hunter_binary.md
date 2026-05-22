# ⚙️ **Reg Hunter Binary**
### `File Name: reg_hunter_binary.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter Binary module to find possible MZ headers in REG_BINARY values

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Binary to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Binary logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Binary timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter Binary module to find possible MZ headers in REG_BINARY values
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 6a4235ed-7288-43b3-8750-f404aa85ed6a
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --binary --outfile %destinationDirectory%\reg_hunter_binary.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
