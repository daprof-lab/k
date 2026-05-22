# ⚙️ **Recmd All Batch Files**
### `File Name: RECmd_AllBatchFiles.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
RECmd: All RECmd Batch Output

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Recmd All Batch Files to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Recmd All Batch Files logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Recmd All Batch Files timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RECmd: All RECmd Batch Output'
Category: Registry
Author: Andrew Rathbun
Version: 1.2
Id: f2c9c95d-375e-4fb7-b069-7e9b95ea6db5
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/RegistryExplorer_RECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: RECmd_AllRegExecutablesFoundOrRun.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_BasicSystemInfo.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_BCDBootVolume.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_InstalledSoftware.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_DFIRBatch.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_RECmd_Batch_MC.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_RegistryASEPs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_SoftwareASEPs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_SoftwareClassesASEPs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_SoftwareWoW6432ASEPs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_SystemASEPs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_UserActivity.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RECmd_UserClassesASEPs.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://github.com/EricZimmerman/RECmd
# https://binaryforay.blogspot.com/2015/05/introducing-recmd.html
# https://aboutdfir.com/toolsandartifacts/windows/registry-explorer-recmd/
# https://www.andreafortuna.org/2020/03/04/recmd-command-line-tool-for-windows-registry-analysis/
# https://www.sans.org/blog/finding-registry-malware-persistence-with-recmd/
# https://www.youtube.com/watch?v=tk9XsMHzPlM
# https://www.youtube.com/watch?v=GhCZfCzn2l0
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
