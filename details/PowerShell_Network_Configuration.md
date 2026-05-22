# ⚙️ **Power Shell Network Configuration**
### `File Name: PowerShell_Network_Configuration.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract Network Configuration via PowerShell

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Network Configuration to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Network Configuration logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Network Configuration timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract Network Configuration via PowerShell
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 634139bf-238a-4891-95e9-5d1b9c4e137d
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter IPEnabled=TRUE | Select Index, ServiceName, Description, MacAddress, @{Name='IpAddress';Expression={$_.IpAddress -join '; '}}, @{Name='DefaultIPGateway';Expression={$_.DefaultIPGateway -join '; '}}, DnsHostname, DnsDomain, DhcpEnabled, DhcpServer, DHCPLeaseObtained | Sort-Object Index | Export-Csv %destinationDirectory%\Network_Configuration.csv"
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-netipconfiguration?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
