# ⚙️ **Power Shell Convert Usage Logs To CSV**
### `File Name: PowerShell_ConvertUsageLogsTo-CSV.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ConvertUsageLogsTo-CSV.ps1 - Export the Usage Logs file(s) into a single CSV file.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Convert Usage Logs To CSV to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Convert Usage Logs To CSV logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Convert Usage Logs To CSV timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: ConvertUsageLogsTo-CSV.ps1 - Export the Usage Logs file(s) into a single CSV file.
Category: ProgramExecution
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: 6fb52c8b-f325-4c08-b9cc-5aa11285b161
BinaryUrl: https://gist.github.com/Qazeer/6c655627962f034aa2b6e92594770ee2
ExportFormat: CSV
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\ConvertUsageLogsTo-CSV.ps1' -InputDir '%sourceDirectory%' -Destination %destinationDirectory%"
        ExportFormat: CSV

# Documentation
# https://gist.github.com/Qazeer/6c655627962f034aa2b6e92594770ee2
# Convert Usage Logs file(s) from the specified Source Directory into a single CSV file.
# Original script and KAPE module to copy the ConsoleHost_history.txt files from Andrew Rathbun and Matt Arbaugh.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
