# ⚙️ **Power Shell Convert Pshistory To CSV**
### `File Name: PowerShell_ConvertPSHistoryTo-CSV.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ConvertPSHistoryTo-CSV.ps1 - Export the ConsoleHost_history.txt file(s) into a single CSV file.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Convert Pshistory To CSV to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Convert Pshistory To CSV logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Convert Pshistory To CSV timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: ConvertPSHistoryTo-CSV.ps1 - Export the ConsoleHost_history.txt file(s) into a single CSV file.
Category: ProgramExecution
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: bab1fd35-90f6-45b7-913b-32ac71b45ea7
BinaryUrl: https://gist.github.com/Qazeer/a0c1c14bb1eae233c1147d1d9dfb3e93
ExportFormat: CSV
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\ConvertPSHistoryTo-CSV.ps1' -InputDir '%sourceDirectory%' -Destination %destinationDirectory%"
        ExportFormat: CSV

# Documentation
# https://gist.github.com/Qazeer/a0c1c14bb1eae233c1147d1d9dfb3e93
# Convert ConsoleHost_history.txt files from the specified Source Directory into a single CSV file.
# Original script and KAPE module to copy the ConsoleHost_history.txt files from Andrew Rathbun and Matt Arbaugh.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
