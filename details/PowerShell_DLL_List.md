# ⚙️ **Power Shell DLL List**
### `File Name: PowerShell_DLL_List.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** nov3mb3r, JorZay  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
DLL List

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell DLL List to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell DLL List logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell DLL List timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: DLL List
Category: LiveResponse
Author: nov3mb3r, JorZay
Version: 1.1
Id: 19e6448f-f94b-49a4-bc16-26080b7c0592
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "gps | Format-List ProcessName, @{l=\"Modules\";e={$_.Modules|Out-String}}"
        ExportFormat: txt
        ExportFile: dlllist.txt

# Documentation
# https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-process?view=powershell-7.2
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
