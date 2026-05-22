# ⚙️ **Power Shell Smbmapping**
### `File Name: PowerShell_SMBMapping.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano, Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Retrieves the Server Message Block (SMB) client directory mappings. It replaces the command net use.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Smbmapping to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Smbmapping logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Smbmapping timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Retrieves the Server Message Block (SMB) client directory mappings. It replaces the command net use.
Category: Network Activity
Author: Vito Alfano, Max Zabuty
Version: 1.0
Id: 36092684-5d40-4159-baed-822b7eaaf0a0
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBMapping | Select LocalPath, RemotePath, Status, RequireIntegrity, RequirePrivacy, UseWriteThrough | Export-Csv -NoTypeInformation -Encoding UTF8 -Path '%destinationDirectory%\SMB Mapping.csv' "
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBMapping | Select LocalPath, RemotePath, Status, RequireIntegrity, RequirePrivacy, UseWriteThrough | Export-Csv -NoTypeInformation -Encoding UTF8 -Path '%destinationDirectory%\SMB Mapping.json' "
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/smbshare/get-smbmapping?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
