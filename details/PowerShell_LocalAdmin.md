# ⚙️ **Power Shell Local Admin**
### `File Name: PowerShell_LocalAdmin.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers detailed list of local admin users

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Local Admin to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Local Admin logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Local Admin timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers detailed list of local admin users
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: d5d3ebba-e95b-456b-90e9-97c18f95d43c
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command " Get-LocalGroupMember -Group "Administrators" | Select Name, SID, PrincipalSource, Description | Export-Csv -Path %destinationDirectory%\Local_Admin_List.csv -NoTypeInformation "
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.localaccounts/get-localgroupmember?view=powershell-5.1
# https://activedirectorypro.com/find-local-administrators-on-all-computers/
# https://powershellguru.com/get-localgroupmember/
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
