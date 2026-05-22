# ⚙️ **Power Shell Execute Bmc Tools**
### `File Name: PowerShell_Execute-BmcTools.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute-BmcTools.ps1 - Recursively process the specified input folder to execute bmc-tools.exe over each Bitmap Cache subfolder(s) found.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Execute Bmc Tools to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Execute Bmc Tools logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Execute Bmc Tools timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute-BmcTools.ps1 - Recursively process the specified input folder to execute bmc-tools.exe over each Bitmap Cache subfolder(s) found.
Category: RemoteAccess
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: 5ac4cc42-cbf4-4862-9d4a-083ea5a16a28
BinaryUrl: https://gist.github.com/Qazeer/3a6d43a117bbece6d83e7e79687e0870
ExportFormat: bmp
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Execute-BmcTools.ps1' -bmcToolsBinary '%kapeDirectory%\\Modules\\bin\\bmc-tools.exe' -InputDir '%sourceDirectory%' -OutputDir '%destinationDirectory%'"
        ExportFormat: bmp

# Documentation
# Recursively process the specified input folder to execute bmc-tools.exe over each Bitmap Cache subfolder(s) found.
# bmc-tools is a Python RDP Bitmap Cache parser from ANSSI (https://github.com/ANSSI-FR/bmc-tools).
# bmc-tools.exe (https://github.com/Qazeer/bmc-tools-compiled/releases/download/v3.02/bmc-tools.exe) is a compiled version of the bmc-tools.py that must be placed under "%kapeDirectory%\Modules\bin\bmc-tools.exe".
# Execute-BmcTools.ps1 (https://gist.github.com/Qazeer/3a6d43a117bbece6d83e7e79687e0870) is basically a wrapper to make bmc-tools.exe output results to user specific folders.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
