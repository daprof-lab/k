# ⚙️ **Power Shell Processes Including Services**
### `File Name: PowerShell_ProcessesIncludingServices.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Processes list including the services running them

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Processes Including Services to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Processes Including Services logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Processes Including Services timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Processes list including the services running them
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: 021ed07e-f2ea-4ec7-9eba-bc1e1576aa46
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "tasklist /svc /FO csv  | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Process_Including_Services.csv'"
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tasklist
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
