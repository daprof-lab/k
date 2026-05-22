# ⚙️ **Reg Hunter Url**
### `File Name: reg_hunter_url.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute Reghunter URL module to find URLs

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reg Hunter Url to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reg Hunter Url logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reg Hunter Url timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute Reghunter URL module to find URLs
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 36786dd5-da30-4acc-a055-c22f79e744e2
BinaryUrl: https://github.com/theflakes/reg_hunter/
ExportFormat: json
Processors:
    -
        Executable: Reghunter\reg_hunter-64.exe
        CommandLine: -a --url --outfile %destinationDirectory%\reg_hunter_url.json
        ExportFormat: json

# Documentation
# https://github.com/theflakes/reg_hunter/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
