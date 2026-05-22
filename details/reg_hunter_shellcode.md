# ⚙️ **Reg Hunter Shellcode**
### `File Name: reg_hunter_shellcode.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter Shellcode to find possible shellcode

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Shellcode to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Shellcode logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Shellcode timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter Shellcode to find possible shellcode
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 67925c73-a5ed-4e4d-97c4-6d6b757f3037
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --shellcode --outfile %destinationDirectory%\reg_hunter_shellcode.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
