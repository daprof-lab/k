# ⚙️ **SOFELK Parser Evtx Ecmd**
### `File Name: SOFELK_Parser_EvtxECmd.mkape`

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
* **Bulk Automated Parsing**: Run SOFELK Parser Evtx Ecmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SOFELK Parser Evtx Ecmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SOFELK Parser Evtx Ecmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing for SOF-ELK Instance
Category: SOF-ELK
Author: Tony Knutson and Andrew Rathbun
Version: 1.0
Id: 7e5e99c0-c97e-485a-baa9-3a284852bc69
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/EvtxExplorer.zip
ExportFormat: json
Processors:
    -
        Executable: EvtxECmd\EvtxECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory%
        ExportFormat: json

# Documentation
# https://aboutdfir.com/sof-elk-and-integration-with-kape/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
