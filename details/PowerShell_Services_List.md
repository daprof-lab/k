# ⚙️ **Power Shell Services List**
### `File Name: PowerShell_Services_List.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Retrieves basic information about active running services. It replaces the command net start.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Services List to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Services List logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Services List timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Retrieves basic information about active running services. It replaces the command net start.
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: fc09e7c4-8af0-4177-8824-a69ad0aa10bf
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-Service | Where-Object {$_.Status -eq 'Running'} | Select-Object -Property Name, DisplayName, Status  | Export-Csv -Path %destinationDirectory%\Services.csv -NoTypeInformation "
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-service?view=powershell-7.3
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
