# ⚙️ **Kernel Dump**
### `File Name: KernelDump.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
This script allows you to dump the Kernel part of the ram without using any external tool.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Kernel Dump to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Kernel Dump logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Kernel Dump timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: This script allows you to dump the Kernel part of the ram without using any external tool.
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: d0c41676-d348-439b-9f08-4af87c1c447d
BinaryUrl: https://raw.githubusercontent.com/conexioninversa/Forensics/master/KernelDump.ps1
ExportFormat: FileSystem
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -ep bypass -Command %kapedirectory%\Modules\bin\KernelDump.ps1 %destinationDirectory%
        ExportFormat: FileSystem

# Documentation
# Where the Microsoft Storage namespace is available (known not to be available in Win7), PowerShell can be used to invoke a native live memory dump
# The result generates a "Kernel.dmp" file
## Special thanks to Grzegorz Tworek - 0gtweet.
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
