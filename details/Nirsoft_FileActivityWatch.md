# ⚙️ **Nirsoft File Activity Watch**
### `File Name: Nirsoft_FileActivityWatch.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
FileActivityWatch is a tool for Windows that displays information about every read/write/delete operation of files occurs on your system. For every file, FileActivityWatch displays the number of read/write bytes, number of read/write/delete operations, first and last read/write timestamp, and the name/ID of the process responsible for the file operation.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft File Activity Watch to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft File Activity Watch logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft File Activity Watch timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: FileActivityWatch is a tool for Windows that displays information about every read/write/delete operation of files occurs on your system. For every file, FileActivityWatch displays the number of read/write bytes, number of read/write/delete operations, first and last read/write timestamp, and the name/ID of the process responsible for the file operation.
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: b766fc10-179e-431b-a3bd-062537dfd294
BinaryUrl: https://www.nirsoft.net/utils/fileactivitywatch-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: FileActivityWatch.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_FileActivityWatch.csv
        ExportFormat: csv

# Documentation
# tool for Windows that displays information about every read/write/delete operation of files occurs on your system. For every file, FileActivityWatch displays the number of read/write bytes, number of read/write/delete operations, first and last read/write timestamp, and the name/ID of the process responsible for the file operation.
# https://www.nirsoft.net/utils/file_activity_watch.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
