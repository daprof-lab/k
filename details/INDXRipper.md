# ⚙️ **Indxripper**
### `File Name: INDXRipper.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Harel Segev  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
INDXRipper: parse all $I30s from live system

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Indxripper to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Indxripper logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Indxripper timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'INDXRipper: parse all $I30s from live system'
Category: FileSystem
Author: Harel Segev
Version: 1.0
Id: 7fc17392-ebd6-4b10-b8d4-55d67dc010a2
BinaryUrl: https://github.com/harelsegev/INDXRipper/releases
ExportFormat: csv
Processors:
    -
        Executable: INDXRipper\INDXRipper.exe
        CommandLine: --deleted-dirs \\.\%sourceDriveLetter% %destinationDirectory%\INDXRipper_All.csv
        ExportFormat: csv

# Documentation
# https://github.com/harelsegev/INDXRipper
# Create a folder "INDXRipper" within the "Modules\bin" KAPE folder
# Extract the contents of "INDXRipper-5.2.6-py3.9-amd64.zip" into "Modules\bin\INDXRipper"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
