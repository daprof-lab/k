# ⚙️ **SOF-ELK Processing Sync**
### `File Name: SOFELK_Parser.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Tony Knutson / Andrew Rathbun  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Prepares and parses extracted forensic artifacts to facilitate ingestion into a SOF-ELK server.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run SOF-ELK Processing Sync to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SOF-ELK Processing Sync logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SOF-ELK Processing Sync timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing for SOF-ELK Instance
Category: SOF-ELK
Author: Tony Knutson and Andrew Rathbun
Version: 1.2
Id: ae3ce0ae-1531-4916-a448-2fa2039fb714
BinaryUrl: https://ericzimmerman.github.io/
ExportFormat: json
Processors:
    -
        Executable: SOFELK_Parser_EvtxECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SOFELK_Parser_LEcmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SOFELK_Parser_MFTECmd_MFT.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SOFELK_Parser_MFTECmd_J.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SOFELK_Parser_PECmd.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://aboutdfir.com/sof-elk-and-integration-with-kape/
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
