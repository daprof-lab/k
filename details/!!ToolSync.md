# ⚙️ **KAPE ToolSync Script**
### `File Name: !!ToolSync.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun / Andreas Hunkeler  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Automates checking Github repositories to update local KAPE maps, targets, and modules.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run KAPE ToolSync Script to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw KAPE ToolSync Script logs to index file anomalies.
* **Incident Impact Assessment**: Leverage KAPE ToolSync Script timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Sync for new Maps, Batch Files, Targets and Modules'
Category: Sync
Author: Andrew Rathbun, Andreas Hunkeler (@Karneades)
Version: 1.0
Id: 8d0a44a4-fa8e-443b-8f6e-8711ce2acd12
BinaryUrl: See different tool Modules
ExportFormat: ""
Processors:

    -
        Executable: Sync_EvtxECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Sync_KAPE.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Sync_RECmd.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Sync_SQLECmd.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://github.com/EricZimmerman/
# This Module ensures you have the latest RECmd Batch files, EVTXECmd Maps, SQLECmd Maps, and KAPE Targets/Modules.
# Ensure you use the tool version which provides the sync option.
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
