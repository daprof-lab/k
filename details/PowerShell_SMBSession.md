# ⚙️ **Power Shell Smbsession**
### `File Name: PowerShell_SMBSession.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano, Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Retrieves basic information about active SMB sessions. It replaces the command net use.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Smbsession to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Smbsession logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Smbsession timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Retrieves basic information about active SMB sessions. It replaces the command net use.
Category: Network Activity
Author: Vito Alfano, Max Zabuty
Version: 1.0
Id: 3d38b9bb-64dd-440e-9a01-8db0feceb3a7
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBSession | Select SessionId, ClientComputerName, ClientUserName, NumOpens  | Export-Csv -NoTypeInformation -Encoding UTF8 -Path '%destinationDirectory%\SMB Session.csv' "
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBSession | Select SessionId, ClientComputerName, ClientUserName, NumOpens | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath 'SMB Session.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/smbshare/get-smbsession?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
