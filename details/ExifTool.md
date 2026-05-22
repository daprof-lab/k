# ⚙️ **Exif Tool**
### `File Name: ExifTool.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Lee Whitfield/esecrpm  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Exiftool: process files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Exif Tool to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Exif Tool logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Exif Tool timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Exiftool: process files'
Category: ExifData
Author: Lee Whitfield/esecrpm
Version: 1.1
Id: 75c32df2-8dad-4bbc-9230-2c3749fd6e2a
BinaryUrl: https://exiftool.org/exiftool-12.29.zip
ExportFormat: csv
Processors:
   -
      Executable: exiftool.exe
      CommandLine: -r %sourceDirectory% -csv
      ExportFormat: csv
      ExportFile: exif.csv

# Documentation
# https://exiftool.org/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
