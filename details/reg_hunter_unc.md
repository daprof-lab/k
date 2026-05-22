# ⚙️ **Reg Hunter Unc**
### `File Name: reg_hunter_unc.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter UNC module to find UNC paths

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Unc to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Unc logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Unc timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter UNC module to find UNC paths
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 78bb9543-80df-45fc-aef5-1f560702529e
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --unc --outfile %destinationDirectory%\reg_hunter_unc.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
