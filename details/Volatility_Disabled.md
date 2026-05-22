# ⚙️ **Volatility Disabled**
### `File Name: Volatility_Disabled.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Jos Clephas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Post-Process memory images with Volatility. The mkape files in this file are disabled by-default because the Volatility plugins have a high runtime and most of them are commonly not used for triage.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Volatility Disabled to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Volatility Disabled logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Volatility Disabled timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Post-Process memory images with Volatility. The mkape files in this file are disabled by-default because the Volatility plugins have a high runtime and most of them are commonly not used for triage.
Category: Modules
Author: Jos Clephas
Version: 1.0
Id: aa982fb9-dc79-4e42-85d8-34079ef9271c
BinaryUrl: http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_win64_standalone.zip
ExportFormat: greptext
Processors:
    -
        Executable: Volatility_apihooks.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_dlldump.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_dumpfiles.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_filescan.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_handles.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_malfind_dump.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_memdump.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_mftparser.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_moddump.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_procdump.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_shellbags.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: Volatility_timeliner.mkape
        CommandLine: ""
        ExportFormat: ""

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
