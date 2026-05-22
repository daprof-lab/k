# ⚙️ **Power Shell Smbopen File**
### `File Name: PowerShell_SMBOpenFile.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano, Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Retrieves basic information about the files that are open via SMB

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Smbopen File to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Smbopen File logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Smbopen File timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Retrieves basic information about the files that are open via SMB
Category: Network Activity
Author: Vito Alfano, Max Zabuty
Version: 1.0
Id: f93f31dc-2979-4279-b1f7-a4771b7ed1fa
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBOpenFile | Select FileId, SessionId, Path, ShareRelativePath, ClientComputerName, ClientUsername | Export-Csv -NoTypeInformation -Encoding UTF8 -Path '%destinationDirectory%\SMB Open Files.csv' "
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBOpenFile | Select FileId, SessionId, Path, ShareRelativePath, ClientComputerName, ClientUsername | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\SMB Open Files.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/smbshare/get-smbopenfile?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
