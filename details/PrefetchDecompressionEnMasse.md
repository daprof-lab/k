# ⚙️ **Prefetch Decompression En Masse**
### `File Name: PrefetchDecompressionEnMasse.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Nisarg Suthar  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Prefetch Decompression En Masse

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Prefetch Decompression En Masse to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Prefetch Decompression En Masse logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Prefetch Decompression En Masse timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Prefetch Decompression En Masse
Category: ProgramExecution
Author: Nisarg Suthar
Version: 1.0
Id: 857e3887-7d80-47da-9d0f-93e7187938cb
BinaryUrl: https://github.com/nisargsuthar/PrefetchDecompressionEnMasse/releases/download/v1.3/PrefetchDecompressionEnMasse.exe
ExportFormat: pf
FileMask: "*.pf"
Processors:
    -
        Executable: PrefetchDecompressionEnMasse.exe
        CommandLine: "%sourceDirectory% %destinationDirectory%"
        ExportFormat: pf

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
