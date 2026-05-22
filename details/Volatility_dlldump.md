# ⚙️ **Volatility Dlldump**
### `File Name: Volatility_dlldump.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Jos Clephas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Post-Process memory images with Volatility

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Volatility Dlldump to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Volatility Dlldump logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Volatility Dlldump timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Post-Process memory images with Volatility
Category: Memory
Author: Jos Clephas
Version: 1.0
Id: f611f68a-1248-42ca-b3d4-8e88469ce586
BinaryUrl: http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_win64_standalone.zip
ExportFormat: greptext
Processors:
    -
        Executable: volatility_2.6_win64_standalone.exe
        CommandLine: -f %sourceDirectory%\memory.dmp dlldump --output=greptext --output-file=%destinationDirectory%\volatility_dlldump.txt --dump-dir=%destinationDirectory%
        ExportFormat: greptext

# Documentation
# https://github.com/volatilityfoundation/volatility
# https://github.com/volatilityfoundation/volatility/wiki
# https://resources.infosecinstitute.com/topic/memory-forensics-and-analysis-using-volatility/
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
