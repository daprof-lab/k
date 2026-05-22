# ⚙️ **Power Shell Network Adapters**
### `File Name: PowerShell_NetworkAdapters.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collecting Network Adapters Information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Network Adapters to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Network Adapters logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Network Adapters timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collecting Network Adapters Information
Category: Network Activity
Author: Max Zabuty
Version: 1.0
Id: 15ab571c-1fde-433e-a9b7-9132542ff07f
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetAdapter | Select Name, Status, MacAddress, PhysicalMediaType, DriverName, DriverInformation, DriverVersion, DriverDescription, SystemName, PnPDeviceID | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Network Adapters.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetAdapter | Select Name, Status, MacAddress, PhysicalMediaType, DriverName, DriverInformation, DriverVersion, DriverDescription, SystemName, PnPDeviceID | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Network Adapters.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/netadapter/get-netadapter?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
