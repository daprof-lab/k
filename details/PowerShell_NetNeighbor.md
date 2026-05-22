# ⚙️ **Power Shell Net Neighbor**
### `File Name: PowerShell_NetNeighbor.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Displaying ARP Table using PowerShell

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Net Neighbor to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Net Neighbor logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Net Neighbor timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Displaying ARP Table using PowerShell
Category: Network Activity
Author: Max Zabuty
Version: 1.0
Id: f25cbff9-fb0c-406b-ba70-c61709c102ae
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetNeighbor | ?{$_.AddressFamily -eq 'IPv4'} | Select InterfaceAlias,IPAddress,LinkLayerAddress,State | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\ARP Table.csv' "
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetNeighbor | ?{$_.AddressFamily -eq 'IPv4'} | Select InterfaceAlias,IPAddress,LinkLayerAddress,State | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\ARP Table.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-netneighbor?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
