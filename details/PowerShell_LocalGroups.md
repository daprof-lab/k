# ⚙️ **Power Shell Local Groups**
### `File Name: PowerShell_LocalGroups.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Local Groups List

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Local Groups to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Local Groups logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Local Groups timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Local Groups List
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: e753b244-382b-4143-976e-1968c5b38973
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-LocalGroup | select * | Export-Csv -Encoding UTF8 -NoTypeInformation -Path '%destinationDirectory%\Local Groups.csv'"
        ExportFormat: csv
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-LocalGroup | select * | ConvertTo-Json | Out-File -Encoding UTF8 -FilePath '%destinationDirectory%\Local Groups.json'"
        ExportFormat: json

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.localaccounts/get-localgroup?view=powershell-5.1
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
