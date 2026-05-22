# ⚙️ **Power Shell Network Connections Status**
### `File Name: PowerShell_Network_Connections_Status.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract Network Connections details via powershell

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Network Connections Status to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Network Connections Status logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Network Connections Status timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract Network Connections details via powershell
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: a47d0af8-842a-4e22-8fba-94688e2dc097
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetTCPConnection | select Local*, Remote*, State, @{n='ProcessName';e={(Get-Process -Id $_.OwningProcess).ProcessName}}, @{n='ProcessPath';e={(Get-Process -Id $_.OwningProcess).Path}} | Export-Csv %destinationDirectory%\Network_Connection_Status.csv -NoTypeInformation"
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-nettcpconnection?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
