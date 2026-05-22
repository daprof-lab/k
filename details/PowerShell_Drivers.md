# ⚙️ **Power Shell Drivers**
### `File Name: PowerShell_Drivers.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Drivers List

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Drivers to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Drivers logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Drivers timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Drivers List
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: 81690a49-c71f-4913-9fb9-430ffa47b413
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-WmiObject -Class Win32_SystemDriver | Select DisplayName,Name,Description,State,PathName,ServiceType | Export-Csv -NoTypeInformation -Path '%destinationDirectory%\Drivers.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-WmiObject -Class Win32_SystemDriver | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Drivers.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/windows/win32/cimwin32prov/win32-systemdriver
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
