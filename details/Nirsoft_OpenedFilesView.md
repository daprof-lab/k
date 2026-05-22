# ⚙️ **Nirsoft Opened Files View**
### `File Name: Nirsoft_OpenedFilesView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_OpenedFilesView.exe - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Opened Files View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Opened Files View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Opened Files View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_OpenedFilesView.exe - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 18e756b8-48ac-4ba9-861e-21099f9833a6
BinaryUrl: https://www.nirsoft.net/utils/ofview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: OpenedFilesView.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_OpenedFilesView.csv /sort "Process name"
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/opened_files_view.html
# OpenedFilesView displays the list of all opened files on your system. For each opened file, additional information is displayed: handle value, read/write/delete access, file position, the process that opened the file, and more...
# Optionally, you can also close one or more opened files, or close the process that opened these files.
# This utility is especially useful if you try to delete/move/open a file
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
