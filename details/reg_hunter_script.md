# ⚙️ **Reg Hunter Script**
### `File Name: reg_hunter_script.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter Script module to find script files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Script to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Script logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Script timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter Script module to find script files
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 44485205-d803-4fb3-b4b5-8fe050bb0cda
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --script --outfile %destinationDirectory%\reg_hunter_script.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
