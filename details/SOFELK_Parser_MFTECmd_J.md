# ⚙️ **SOFELK Parser Mftecmd J**
### `File Name: SOFELK_Parser_MFTECmd_J.mkape`

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
* **Bulk Automated Parsing**: Run SOFELK Parser Mftecmd J to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SOFELK Parser Mftecmd J logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SOFELK Parser Mftecmd J timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing for SOF-ELK Instance
Category: SOF-ELK
Author: Tony Knutson and Andrew Rathbun
Version: 1.0
Id: a3c8f694-b20e-43aa-96e5-3a5df2379321
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/MFTECmd.zip
ExportFormat: json
FileMask: $J
Processors:
    -
        Executable: MFTECmd.exe
        CommandLine: -f %sourceFile% --json %destinationDirectory%
        ExportFormat: json

# Documentation
# https://aboutdfir.com/sof-elk-and-integration-with-kape/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
