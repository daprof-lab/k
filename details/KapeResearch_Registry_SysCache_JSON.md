# ⚙️ **Kape Research Registry Sys Cache JSON**
### `File Name: KapeResearch_Registry_SysCache_JSON.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RECmd: Convert SysCache Registry hive to JSON for research

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Kape Research Registry Sys Cache JSON to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Kape Research Registry Sys Cache JSON logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Kape Research Registry Sys Cache JSON timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RECmd: Convert SysCache Registry hive to JSON for research'
Category: KapeResearch
Author: Andrew Rathbun
Version: 1.0
Id: e867ca47-0938-4f10-8aad-3f5aa2240222
BinaryUrl: https://f001.backblazeb2.com/file/EricZimmermanTools/RegistryExplorer_RECmd.zip
ExportFormat: json
FileMask: SysCache
Processors:
    -
        Executable: RECmd\RECmd.exe
        CommandLine: -f %sourceFile% --kn ROOT --nl false --json %destinationDirectory% --jsonf SysCache.json
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/RECmd
# https://binaryforay.blogspot.com/2015/05/introducing-recmd.html
# https://aboutdfir.com/toolsandartifacts/windows/registry-explorer-recmd/
# https://www.andreafortuna.org/2020/03/04/recmd-command-line-tool-for-windows-registry-analysis/
# https://www.sans.org/blog/finding-registry-malware-persistence-with-recmd/
# https://www.youtube.com/watch?v=tk9XsMHzPlM
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# Note: --nl false replays transaction logs. If you don't want to replay transaction logs, change to --nl true.
# This Module will convert the entire content any registry hives into JSON, which is helpful for viewing all that the hives contain in an easily searchable way
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
