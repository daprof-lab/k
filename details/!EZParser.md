# ⚙️ **EZParser Compound Suite**
### `File Name: !EZParser.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Phill Moore  
**Version:** 1.5
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs all Eric Zimmerman analytical tools consecutively against their respective targets.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run EZParser Compound Suite to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw EZParser Compound Suite logs to index file anomalies.
* **Incident Impact Assessment**: Leverage EZParser Compound Suite timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Eric Zimmerman Parsers
Category: Modules
Author: Phill Moore
Version: 1.5
Id: f531e7cc-c9f3-4d04-881b-dbc89d1e7f38
BinaryUrl: https://ericzimmerman.github.io/
ExportFormat: csv
Processors:
    -
        Executable: AmcacheParser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: AppCompatCacheParser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: EvtxECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: JLECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: LECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: MFTECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: PECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RBCmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RecentFileCacheParser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_DFIRBatch.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SBECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SQLECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SrumECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: SumECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: WxTCmd.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://www.youtube.com/watch?v=GhCZfCzn2l0
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
