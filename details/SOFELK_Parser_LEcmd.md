# ⚙️ **SOFELK Parser Lecmd**
### `File Name: SOFELK_Parser_LEcmd.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Tony Knutson and Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parsing for SOF-ELK Instance

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run SOFELK Parser Lecmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SOFELK Parser Lecmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SOFELK Parser Lecmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing for SOF-ELK Instance
Category: SOF-ELK
Author: Tony Knutson and Andrew Rathbun
Version: 1.0
Id: 1544a0ef-63de-4229-8dab-d9b36b9f95fe
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/LECmd.zip
ExportFormat: json
Processors:
    -
        Executable: LECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory% -q
        ExportFormat: json

# Documentation
# https://aboutdfir.com/sof-elk-and-integration-with-kape/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
