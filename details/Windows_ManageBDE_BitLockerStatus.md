# ⚙️ **Windows Manage BDE Bit Locker Status**
### `File Name: Windows_ManageBDE_BitLockerStatus.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** troyla@microsoft.com  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Check for BitLocker volumes

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Manage BDE Bit Locker Status to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Manage BDE Bit Locker Status logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Manage BDE Bit Locker Status timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Check for BitLocker volumes
Category: VolumeInformation
Author: troyla@microsoft.com
Version: 1.1
Id: b069705b-13f0-42c7-86a2-4f310c3c651b
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\manage-bde.exe
        CommandLine: -status %sourceDriveLetter%
        ExportFormat: txt
        ExportFile: BitLocker-Status.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/manage-bde
# Updated to directly reference the system path
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
