# ⚙️ **Power Shell Local Users**
### `File Name: PowerShell_LocalUsers.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Local Users List

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Local Users to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Local Users logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Local Users timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Local Users List
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: 1bce3dc1-72d5-4b5d-9ca9-c15745aadc7e
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-LocalUser | select * | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Local Users.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-LocalUser | select * | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Local Users.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.localaccounts/get-localuser?view=powershell-5.1
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
