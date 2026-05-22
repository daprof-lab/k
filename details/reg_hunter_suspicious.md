# ⚙️ **Reg Hunter Suspicious**
### `File Name: reg_hunter_suspicious.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter Suspicious module to find various suspicious substrings (e.g. iex, invoke-expression, etc.)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Suspicious to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Suspicious logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Suspicious timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter Suspicious module to find various suspicious substrings (e.g. iex, invoke-expression, etc.)
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 92bbd283-8446-46db-b0d2-eb8068c627fd
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --suspicious --outfile %destinationDirectory%\reg_hunter_suspicious.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
