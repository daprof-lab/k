# ⚙️ **Power Shell Defender Exclusions**
### `File Name: PowerShell_Defender_Exclusions.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** nov3mb3r  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Defender Exclusions

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Defender Exclusions to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Defender Exclusions logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Defender Exclusions timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Windows Defender Exclusions
Category: LiveResponse
Author: nov3mb3r
Version: 1.0
Id: 5a9ce674-0d3c-4c9a-9f53-d0130bb4aafb
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\Windows Defender\Exclusions'"
        ExportFormat: txt
        ExportFile: defenderexclusions.txt

# Documentation
# https://docs.microsoft.com/en-us/powershell/scripting/samples/working-with-registry-entries?view=powershell-7.2
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
