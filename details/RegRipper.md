# ⚙️ **RegRipper Hive Parser**
### `File Name: RegRipper.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** ZeArioch / Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs the RegRipper framework to parse user, system, software, and sam hives using targeted forensic plugins.

---

## 🔍 **Investigative Use-Cases**
* **Automated Registry Auditing**: Extract lists of active services, user accounts, system hostnames, and configuration keys at once.
* **Malicious Persistence Detection**: Scan startup runs, registry autoruns, and scheduler entries to spot active persistent backdoors.
* **User Shellbags Resolution**: Identify directory paths accessed by compromising user accounts by parsing user registry classes.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'RegRipper: parse all supported hives'
Category: Registry
Author: ZeArioch <https://{github,twitter}.com/ZeArioch>, Phill Moore, Andreas Hunkeler (@Karneades)
Version: 1.1
Id: 76037ee9-0346-459a-a44a-1b67edc711c8
BinaryUrl: https://github.com/keydet89/RegRipper3.0
ExportFormat: txt
Processors:
    -
        Executable: RegRipper_SAM.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RegRipper_SECURITY.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RegRipper_SOFTWARE.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RegRipper_SYSTEM.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RegRipper_NTUser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: RegRipper_UsrClass.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# https://github.com/keydet89/RegRipper3.0
# Create a folder "regripper" within the "Modules\bin" KAPE folder
# Place "rip.exe", "p2x5124.dll" and the "plugins" folder into "Modules\bin\regripper"
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
