# ⚙️ **Power Shell Bitlocker Key Extraction**
### `File Name: PowerShell_Bitlocker_Key_Extraction.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extract Bitlocker Key via powershell

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Bitlocker Key Extraction to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Bitlocker Key Extraction logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Bitlocker Key Extraction timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Extract Bitlocker Key via powershell
Category: LiveResponse
Author: Vito Alfano
Version: 1.0
Id: 4339e017-c830-4d54-9de2-4ca726f4aa1a
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-BitLockerVolume -Mountpoint %sourceDriveLetter% | Select-Object -ExpandProperty KeyProtector| Format-List | Out-File -FilePath %destinationDirectory%\Bitlocker_Key.txt"
        ExportFormat: txt

# Documentation
# https://learn.microsoft.com/en-us/powershell/module/bitlocker/get-bitlockervolume?view=windowsserver2022-ps
# https://learn.microsoft.com/en-us/powershell/module/bitlocker/enable-bitlocker?view=windowsserver2022-ps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
