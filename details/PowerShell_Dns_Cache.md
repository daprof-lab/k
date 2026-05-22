# ⚙️ **Power Shell Dns Cache**
### `File Name: PowerShell_Dns_Cache.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract Dns Cache via PowerShell

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Dns Cache to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Dns Cache logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Dns Cache timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract Dns Cache via PowerShell
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 8a0625dc-7f86-4c50-9daf-c99070b46ff2
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-DnsClientCache | Select-Object Entry, Name, Status, Type, TimeToLive, Data | Export-Csv -NoTypeInformation -Path %destinationDirectory%\DnsCache.csv "
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/dnsclient/get-dnsclientcache?view=windowsserver2022-ps
# https://www.iana.org/assignments/dns-parameters/dns-parameters.xhtml - for Status code see the section Resource Record (RR) TYPEs
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
