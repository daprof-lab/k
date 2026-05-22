# ⚙️ **Windows Manage BDE Bit Locker Keys**
### `File Name: Windows_ManageBDE_BitLockerKeys.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** troyla@microsoft.com  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collect BitLocker recovery key for a volume

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Manage BDE Bit Locker Keys to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Manage BDE Bit Locker Keys logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Manage BDE Bit Locker Keys timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collect BitLocker recovery key for a volume
Category: VolumeInformation
Author: troyla@microsoft.com
Version: 1.1
Id: d30abed8-35f3-4fb6-ba47-5ffdad46c912
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\manage-bde.exe
        CommandLine: -protectors -get %sourceDriveLetter%
        ExportFormat: txt
        ExportFile: BitLocker-key.txt

# Documentation
# Updated to directly reference the system path
# NOTE: When using the bitlocker related modules, specify --msource as JUST the drive letter and colon.
# DO NOT include the trailing slash or the command will error out.
# DO this: --msource C:
# NOT this: --msource C:\
# If using targets and not specifying msource, make sure --tsource also uses the same format (no trailing slash)
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
