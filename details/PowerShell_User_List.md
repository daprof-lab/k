# ⚙️ **Power Shell User List**
### `File Name: PowerShell_User_List.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers detailed list of local users

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell User List to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell User List logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell User List timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers detailed list of local users
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 4148dff7-fba3-40e1-a253-a743550ed398
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-WmiObject -Class Win32_UserAccount | Select-Object AccountType, Caption, Domain, Name, FullName, InstallDate, SID, Status | Export-Csv -Path %destinationDirectory%\Local_User_List.csv -NoTypeInformation "
        ExportFormat: csv

# Documentation
# https://learn.microsoft.com/en-us/windows/win32/cimwin32prov/win32-useraccount
# https://www.eightforums.com/threads/user-accounts-view-detailed-information-about-in-windows.50502/
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
