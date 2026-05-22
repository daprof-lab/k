# ⚙️ **Power Shell Net User Administrators**
### `File Name: PowerShell_NetUserAdministrators.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andreas Hunkeler (@Karneades)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command (members of local administrator group)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Net User Administrators to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Net User Administrators logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Net User Administrators timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command (members of local administrator group)
Category: LiveResponse
Author: Andreas Hunkeler (@Karneades)
Version: 1.0
Id: 730cf14e-2680-447f-9853-e79ad3aa0e65
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "$admin = (Get-LocalGroup -Name 'Admini*').name; net localgroup $admin"
        ExportFormat: txt
        ExportFile: NetSystemInfo.txt
        Append: true

# Documentation
# https://docs.microsoft.com/en-us/powershell/?view=powershell-5.1
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
