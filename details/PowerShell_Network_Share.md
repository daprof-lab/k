# ⚙️ **Power Shell Network Share**
### `File Name: PowerShell_Network_Share.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract the list of network shares

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Network Share to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Network Share logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Network Share timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract the list of network shares
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 88e299af-9689-4b8d-ba2d-62e47949ad59
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-SMBShare | select name, volume, path, description | Export-Csv -Path %destinationDirectory%\Network_Share.csv -NoTypeInformation "
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/smbshare/get-smbshare?view=windowsserver2022-ps
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
