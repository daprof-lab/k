# ⚙️ **DNS Client Cache Parser**
### `File Name: PowerShell_DnsClientCache.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts active OS DNS client caches to display recently contacted internet hosts.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run DNS Client Cache Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw DNS Client Cache Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage DNS Client Cache Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Displaying DNS Client Cache
Category: Network Activity
Author: Max Zabuty
Version: 1.0
Id: 0bec8e98-4111-4d91-a774-0b8d50eaf430
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-DnsClientCache | Select Entry,Name,Type,Status,Section,TimeToLive,DataLength,Data | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\DNS Client Cache.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-DnsClientCache | Select Entry,Name,Type,Status,Section,TimeToLive,DataLength,Data | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\DNS Client Cache.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/nettcpip/get-netneighbor?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
