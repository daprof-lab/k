# ⚙️ **SOFELK Parser Mftecmd MFT**
### `File Name: SOFELK_Parser_MFTECmd_MFT.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Tony Knutson and Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parsing for SOF-ELK Instance

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run SOFELK Parser Mftecmd MFT to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SOFELK Parser Mftecmd MFT logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SOFELK Parser Mftecmd MFT timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parsing for SOF-ELK Instance
Category: SOF-ELK
Author: Tony Knutson and Andrew Rathbun
Version: 1.1
Id: bb160156-76b7-4790-83dc-519c06ba53df
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/MFTECmd.zip
ExportFormat: json
FileMask: $MFT
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
