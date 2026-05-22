# ⚙️ **Sync Recmd**
### `File Name: Sync_RECmd.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RECmd: Sync for new Maps

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sync Recmd to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sync Recmd logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sync Recmd timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RECmd: Sync for new Maps'
Category: KAPESync
Author: Andrew Rathbun
Version: 1.1
Id: 3651465e-7165-4705-b7de-ae3006c05db0
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/RegistryExplorer_RECmd.zip
ExportFormat: ""
Processors:
    -
        Executable: RECmd\RECmd.exe
        CommandLine: --sync --debug
        ExportFormat: ""
        ExportFile: Sync_RECmd.txt

# Documentation
# https://github.com/EricZimmerman/RECmd
# https://binaryforay.blogspot.com/2015/05/introducing-recmd.html
# https://aboutdfir.com/toolsandartifacts/windows/registry-explorer-recmd/
# https://www.andreafortuna.org/2020/03/04/recmd-command-line-tool-for-windows-registry-analysis/
# https://www.sans.org/blog/finding-registry-malware-persistence-with-recmd/
# https://www.youtube.com/watch?v=tk9XsMHzPlM
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# This Module ensures you have the latest Batch files for RECmd prior to running RECmd
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
