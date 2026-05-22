# ⚙️ **Dump It Memory ARM**
### `File Name: DumpIt_Memory_ARM.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Doug Metz  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
DumpIt Memory Acquisition for Windows ARM

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Dump It Memory ARM to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Dump It Memory ARM logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Dump It Memory ARM timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: DumpIt Memory Acquisition for Windows ARM
Category: Memory
Author: Doug Metz
Version: 1.2
Id: 35094815-a594-415d-b48f-7437511ea3d1
BinaryUrl: https://www.magnetforensics.com/resources/magnet-dumpit-for-windows/
ExportFormat: dmp
Processors:
    -
        Executable: DumpIt_arm.exe
        CommandLine: /O %destinationDirectory%\memdump.dmp /Q
        ExportFormat: dmp

# Documentation
# The Comae Toolkit includes versions of DumpIt for x86, x64 and ARM. Rename the DumpIt.exe for ARM to DumpIt_arm.exe and save in /modules/bin
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
