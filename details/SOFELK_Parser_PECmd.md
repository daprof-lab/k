# ⚙️ **SOFELK Parser Pecmd**
### `File Name: SOFELK_Parser_PECmd.mkape`

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
* **Bulk Automated Parsing**: Run SOFELK Parser Pecmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SOFELK Parser Pecmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SOFELK Parser Pecmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing for SOF-ELK Instance
Category: SOF-ELK
Author: Tony Knutson and Andrew Rathbun
Version: 1.0
Id: 5da0b20f-4dec-4f6e-8baf-0585f5b1f4d3
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/PECmd.zip
ExportFormat: json
Processors:
    -
        Executable: PECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory% -q
        ExportFormat: json

# Documentation
# https://aboutdfir.com/sof-elk-and-integration-with-kape/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
