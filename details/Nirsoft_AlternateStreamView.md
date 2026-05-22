# ⚙️ **Nirsoft Alternate Stream View**
### `File Name: Nirsoft_AlternateStreamView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_AlternateStreamView - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Alternate Stream View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Alternate Stream View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Alternate Stream View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_AlternateStreamView - Nirsoft'
Category: FileSystem
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: aaa08c93-0dcf-433a-b655-362d9cbce9cb
BinaryUrl: https://www.nirsoft.net/utils/alternatestreamview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: AlternateStreamView.exe
        CommandLine: /scomma %destinationDirectory%\AlternateStreamView.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/alternatestreamview-x64.zip
# AlternateStreamView is a small utility that allows you to scan your NTFS drive, and find all hidden alternate streams stored in the file system
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
