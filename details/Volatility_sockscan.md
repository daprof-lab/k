# ⚙️ **Volatility Sockscan**
### `File Name: Volatility_sockscan.mkape`

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
* **Bulk Automated Parsing**: Run Volatility Sockscan to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Volatility Sockscan logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Volatility Sockscan timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Post-Process memory images with Volatility
Category: Memory
Author: Jos Clephas
Version: 1.0
Id: 3915788a-4513-4951-ac3d-02daaf6a46a9
BinaryUrl: http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_win64_standalone.zip
ExportFormat: greptext
Processors:
    -
        Executable: volatility_2.6_win64_standalone.exe
        CommandLine: -f %sourceDirectory%\memory.dmp dlllist --output=greptext --output-file %destinationDirectory%\volatility_sockscan.txt
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
