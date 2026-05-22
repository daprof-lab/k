# ⚙️ **Recmd User Classes Aseps**
### `File Name: RECmd_UserClassesASEPs.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
RECmd: UserClassesASEPs

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Recmd User Classes Aseps to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Recmd User Classes Aseps logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Recmd User Classes Aseps timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RECmd: UserClassesASEPs'
Category: Registry
Author: Andreas Hunkeler (@Karneades)
Version: 1.1
Id: df3d2d54-dda9-49fb-a427-c9d8348b375d
BinaryUrl: https://download.ericzimmermanstools.com/RECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: RECmd\RECmd.exe
        CommandLine: -d %sourceDirectory% --bn BatchExamples\UserClassesASEPs.reb --nl false --csv %destinationDirectory%
        ExportFormat: csv
        ExportFile: UserClassesASEPs_RECmdConsoleLog.txt

# Documentation
# https://github.com/EricZimmerman/RECmd
# https://binaryforay.blogspot.com/2015/05/introducing-recmd.html
# https://aboutdfir.com/toolsandartifacts/windows/registry-explorer-recmd/
# https://www.andreafortuna.org/2020/03/04/recmd-command-line-tool-for-windows-registry-analysis/
# https://www.sans.org/blog/finding-registry-malware-persistence-with-recmd/
# https://www.youtube.com/watch?v=tk9XsMHzPlM
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# Uses the UserClassesASEPs.reb batch command file. This file should also be in same directory as RECmd.exe
# Note: --nl false replays transaction logs. If you don't want to replay transaction logs, change to --nl true.
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
