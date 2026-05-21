# ⚙️ **Comae DumpIt Memory**
### `File Name: DumpIt_Memory.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Doug Metz  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Triggers high-speed RAM acquisition on a live system to capture running system states.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Comae DumpIt Memory to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Comae DumpIt Memory logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Comae DumpIt Memory timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: DumpIt Memory Acquisition
Category: Memory
Author: Doug Metz
Version: 1.2
Id: 7504551a-41b6-4287-ad8a-ee0a10a66f7d
BinaryUrl: https://www.magnetforensics.com/blog/how-to-get-started-with-comae/
ExportFormat: dmp
Processors:
    -
        Executable: DumpIt.exe
        CommandLine: /O %destinationDirectory%\memdump.dmp /Q
        ExportFormat: dmp

# Documentation
# Comae/DumpIt was rolled into Magnet Idea Lab Info on downloading can be found in this blog:
# https://www.magnetforensics.com/blog/how-to-get-started-with-comae/
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
