# ⚙️ **SANS DeepBlueCLI**
### `File Name: DeepblueCLI.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Garrett Martin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Evaluates Windows Security and System logs to identify credential dumping and user creations.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run SANS DeepBlueCLI to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SANS DeepBlueCLI logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SANS DeepBlueCLI timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Launches SANS DeepBlueCLI against collected Windows Event Logs
Category: EventLogs
Author: Garrett Martin
Version: 1.0
Id: 3fecf23b-077e-4b5b-8ae6-51ad76085e0d
BinaryUrl: https://github.com/sans-blue-team/DeepBlueCLI
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "& '%kapedirectory%\Modules\bin\Process-Deepbluecli.ps1' -scriptLocation %kapedirectory%\Modules\bin\DeepBlueCLI -output '%destinationDirectory%' -source '%sourceDirectory%'"
        ExportFormat: txt

# Documentation
# Obtain deepbluecli files from https://github.com/sans-blue-team/DeepBlueCLI
# Create a folder "DeepBlueCLI" within the "Modules\bin" KAPE folder
# Place the contents from github into "Modules\bin\DeepBlueCLI"
# Acquire Process-Deepbluecli from https://github.com/grrttmrtn1/Process-Deepbluecli
# place Process-Deepbluecli.ps1 in Modules\bin
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
