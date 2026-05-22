# ⚙️ **Reg Hunter Obfuscation**
### `File Name: reg_hunter_obfuscation.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter Obfuscation module to find obfuscated values

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Obfuscation to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Obfuscation logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Obfuscation timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter Obfuscation module to find obfuscated values
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 576ca9cd-30bf-4db2-98a6-7bdd36a9bb13
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --obfuscation --outfile %destinationDirectory%\reg_hunter_obfuscation.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
