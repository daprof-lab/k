# ⚙️ **Power Shell Active Drives**
### `File Name: PowerShell_ActiveDrives.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Active Drives List

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Active Drives to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Active Drives logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Active Drives timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Active Drives List
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: 74d3505a-ec0f-4092-b121-6796583af8e0
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-PSDrive | Select Name,Provider,Root,CurrentLocation | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Active Drives.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-PSDrive | Select Name,Provider,Root,CurrentLocation | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Active Drives.csv'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-psdrive?view=powershell-7.4
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
