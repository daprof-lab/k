# ⚙️ **Power Shell Local Group List**
### `File Name: PowerShell_Local_Group_List.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers detailed list of local groups

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Local Group List to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Local Group List logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Local Group List timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers detailed list of local groups
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 0472b243-8739-4dee-991d-19940ce5bbda
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command " Get-LocalGroup | Select Name, SID, Description | Export-Csv -Path %destinationDirectory%\Local_Group_List.csv -NoTypeInformation "
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.localaccounts/get-localgroupmember?view=powershell-5.1
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
