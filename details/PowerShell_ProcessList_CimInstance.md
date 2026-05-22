# ⚙️ **Power Shell Process List Cim Instance**
### `File Name: PowerShell_ProcessList_CimInstance.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Markus Neis, Swisscom  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Display running processes and context information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Process List Cim Instance to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Process List Cim Instance logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Process List Cim Instance timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Display running processes and context information
Category: LiveResponse
Author: Markus Neis, Swisscom
Version: 1.0
Id: f5afb643-3a77-4e3e-a028-18cbeaf5c406
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-CimInstance Win32_Process | select ProcessId, ProcessName, Path, CommandLine, Description, ParentProcessId , CreationDate, Handle, HandleCount, @{Label='MD5'; Expression={(Get-FileHash -Algorithm MD5 -LiteralPath $_.Path).Hash}} | Export-Csv -NoTypeInformation -Path %destinationDirectory%\PWSH-Get-CIM_ProcessList.csv"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-CimInstance Win32_Process | select ProcessId, ProcessName, Path, CommandLine, Description, ParentProcessId , CreationDate, Handle, HandleCount, @{Label='MD5'; Expression={(Get-FileHash -Algorithm MD5 -LiteralPath $_.Path).Hash}} |  ConvertTo-Json  | Out-File -FilePath %destinationDirectory%\PWSH-Get-CIM_ProcessList.json"
        ExportFormat: json

# Documentation
# https://docs.microsoft.com/en-us/powershell/
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
