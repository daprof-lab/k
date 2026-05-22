# ⚙️ **Power Shell Arp Cache Extraction**
### `File Name: PowerShell_Arp_Cache_Extraction.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract Arp cache via powershell

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Arp Cache Extraction to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Arp Cache Extraction logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Arp Cache Extraction timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract Arp cache via powershell
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 6d22d457-8f8d-4bd0-8045-6af867589dca
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-NetNeighbor | Select-Object InterfaceIndex, InterfaceAlias, IPAddress, State | Sort-Object InterfaceIndex | Export-Csv %destinationDirectory%\Arp_Cache.csv"
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-netneighbor?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
