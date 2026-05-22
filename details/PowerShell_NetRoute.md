# ⚙️ **Power Shell Net Route**
### `File Name: PowerShell_NetRoute.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collecting Network Routing Table Information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Net Route to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Net Route logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Net Route timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collecting Network Routing Table Information
Category: Network Activity
Author: Max Zabuty
Version: 1.0
Id: f1eaaf30-3b13-4c0e-836c-071f7a668948
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: >
            -Command "Get-NetRoute | Select-Object DestinationPrefix, NextHop, InterfaceAlias, RouteMetric, Protocol, InterfaceIndex, AddressFamily | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Network Routing Table.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: >
            -Command "Get-NetRoute | Select-Object DestinationPrefix, NextHop, InterfaceAlias, RouteMetric, Protocol, InterfaceIndex, AddressFamily | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Network Routing Table.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-netroute?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
