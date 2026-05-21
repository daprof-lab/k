# ⚙️ **Volatility hollowfind**
### `File Name: Volatility_hollowfind.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Jos Clephas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Automatically detects process hollowing anomalies and suspicious thread patterns.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Volatility hollowfind to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Volatility hollowfind logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Volatility hollowfind timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Post-Process memory images with Volatility
Category: Memory
Author: Jos Clephas
Version: 1.0
Id: 2d966a97-a950-48b1-8219-e784ffb3a552
BinaryUrl: http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_win64_standalone.zip
ExportFormat: greptext
Processors:
    -
        Executable: volatility_2.6_win64_standalone.exe
        CommandLine: --plugins=.\Custom\VolatilityPlugins -f %sourceDirectory%\memory.dmp hollowfind --output-file=%destinationDirectory%\volatility_hollowfind.txt
        ExportFormat: greptext

# Documentation
# https://github.com/volatilityfoundation/volatility
# https://github.com/volatilityfoundation/volatility/wiki
# https://resources.infosecinstitute.com/topic/memory-forensics-and-analysis-using-volatility/
#
# Place the binary 'volatility_2.6_win64_standalone.exe' into the .\modules\bin folder. And if you want to provide a Volatility profile (such as Win2016x64_14393) or a KDBG, you have to create a file named 'volatilityrc' and place it in the same folder as the Volatility binary. Set the following content in that file:
#
# [DEFAULT]
# PROFILE=Win2016x64_14393
# #KDBG=0x82944c28
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
