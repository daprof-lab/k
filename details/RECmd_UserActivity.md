# ⚙️ **Recmd User Activity**
### `File Name: RECmd_UserActivity.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RECmd: UserActivity

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Recmd User Activity to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Recmd User Activity logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Recmd User Activity timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RECmd: UserActivity'
Category: Registry
Author: Andrew Rathbun
Version: 1.1
Id: 05db97da-327b-46d0-942c-a468c087c09c
BinaryUrl: https://download.ericzimmermanstools.com/RECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: RECmd\RECmd.exe
        CommandLine: -d %sourceDirectory% --bn BatchExamples\UserActivity.reb --nl false --csv %destinationDirectory%
        ExportFormat: csv
        ExportFile: UserActivity_RECmdConsoleLog.txt

# Documentation
# https://github.com/EricZimmerman/RECmd
# https://binaryforay.blogspot.com/2015/05/introducing-recmd.html
# https://aboutdfir.com/toolsandartifacts/windows/registry-explorer-recmd/
# https://www.andreafortuna.org/2020/03/04/recmd-command-line-tool-for-windows-registry-analysis/
# https://www.sans.org/blog/finding-registry-malware-persistence-with-recmd/
# https://www.youtube.com/watch?v=tk9XsMHzPlM
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# Uses the UserActivity.reb batch command file. This file should also be in same directory as RECmd.exe
# Note: --nl false replays transaction logs. If you don't want to replay transaction logs, change to --nl true.
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
