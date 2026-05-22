# ⚙️ **Power Shell Network Ipaddresses**
### `File Name: PowerShell_NetworkIPAddresses.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collecting Network IP Address Information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Network Ipaddresses to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Network Ipaddresses logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Network Ipaddresses timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collecting Network IP Address Information
Category: Network Activity
Author: Max Zabuty
Version: 1.0
Id: 85d5e5cb-630c-4e70-9153-738e30c9d973
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetIPAddress | Select IPAddress,InterfaceAlias,AddressFamily,Type,PrefixLength,PrefixOrigin,SuffixOrigin,AddressState | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Network IP Addresses.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetIPAddress | Select IPAddress,InterfaceAlias,AddressFamily,Type,PrefixLength,PrefixOrigin,SuffixOrigin,AddressState | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Network IP Addresses.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-netipaddress?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
