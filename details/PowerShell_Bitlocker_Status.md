# ⚙️ **Power Shell Bitlocker Status**
### `File Name: PowerShell_Bitlocker_Status.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract Bitlocker status details

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Bitlocker Status to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Bitlocker Status logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Bitlocker Status timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract Bitlocker status details
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 26a2553a-0d60-467b-8e76-94c429f0a20a
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-BitLockerVolume -Mountpoint %sourceDriveLetter% | Format-List | Out-File -FilePath %destinationDirectory%\Bitlocker_Status.txt"
        ExportFormat: txt

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/bitlocker/get-bitlockervolume?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
