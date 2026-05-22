# ⚙️ **Sync Evtx Ecmd**
### `File Name: Sync_EvtxECmd.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
EvtxECmd: Sync for new Maps

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sync Evtx Ecmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sync Evtx Ecmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sync Evtx Ecmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'EvtxECmd: Sync for new Maps'
Category: KAPESync
Author: Andrew Rathbun
Version: 1.1
Id: 43ed0fa4-9d29-44a5-9cfa-3db06e5b5a46
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/EvtxExplorer.zip
ExportFormat: ""
Processors:
    -
        Executable: EvtxECmd\EvtxECmd.exe
        CommandLine: --sync --debug
        ExportFormat: ""
        ExportFile: Sync_EvtxECmd.txt

# Documentation
# https://github.com/EricZimmerman/evtx
# https://binaryforay.blogspot.com/2019/04/introducing-evtxecmd.html
# https://www.youtube.com/watch?v=YvMg3p7O6ro
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# This Module ensures you have the latest Maps prior to parsing event logs with EVTXECmd
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
