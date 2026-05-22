# ⚙️ **Chainsaw MFT Dump**
### `File Name: Chainsaw_MFT_Dump.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Reece394  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Chainsaw: Dump $MFT files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Chainsaw MFT Dump to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Chainsaw MFT Dump logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Chainsaw MFT Dump timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Chainsaw: Dump $MFT files'
Category: FileSystem
Author: Reece394
Version: 1.0
Id: 47e20c2d-eef3-4902-a80d-48aca1329fec
BinaryUrl: https://github.com/WithSecureLabs/chainsaw/releases/latest/download/chainsaw_all_platforms+rules+examples.zip
ExportFormat: json
FileMask: $MFT|*.mft|mft.bin
Processors:
    -
        Executable: Chainsaw\Chainsaw.exe
        CommandLine: dump %sourceFile% --json --output %destinationDirectory%\%d%_MFT_Output.json
        ExportFormat: json

# Documentation
# https://github.com/WithSecureLabs/chainsaw
# Versions of Chainsaw 2.0 and above have changed rule directories
# The Chainsaw executable should reside in .\KAPE\Modules\bin\chainsaw\Chainsaw.exe
# PLEASE NOTE: You may have to rename the Windows executable to Chainsaw.exe manually
# As of posting 11/14/2024 you have to build Chainsaw from source to get $MFT filename support. This will change after v2.10.1.
# Prior versions only support MFT files named with .mft or .bin file extensions.
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
