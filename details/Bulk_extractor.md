# ⚙️ **Bulk Extractor**
### `File Name: Bulk_extractor.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
is a high-performance digital forensics exploitation tool. It is a "get evidence" that rapidly scans any kind of input (disk images, files, directories of files, etc) and extracts structured information such as email addresses, credit card numbers, JPEGs and JSON snippets without parsing the file system or file system structures. The results are stored in text files that are easily inspected, searched, or used as inputs for other forensic processing.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bulk Extractor to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bulk Extractor logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bulk Extractor timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: is a high-performance digital forensics exploitation tool. It is a "get evidence" that rapidly scans any kind of input (disk images, files, directories of files, etc) and extracts structured information such as email addresses, credit card numbers, JPEGs and JSON snippets without parsing the file system or file system structures. The results are stored in text files that are easily inspected, searched, or used as inputs for other forensic processing.
Category: Filemetadata
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: 8340d9a0-0b1a-447e-bc4e-893c66a783ec
BinaryUrl: https://digitalcorpora.s3.amazonaws.com/downloads/bulk_extractor/bulk_extractor-1.5.5-windowsinstaller.exe
ExportFormat: txt
Processors:
    -
        Executable: Bulk_extractor/bulk_extractor.exe
        CommandLine: -o %destinationDirectory% -R %sourceDirectory%
        ExportFormat: txt

# Documentation
# https://github.com/simsong/bulk_extractor/tree/main/doc
# 1)Download the installer from: https://digitalcorpora.s3.amazonaws.com/downloads/bulk_extractor/bulk_extractor-1.5.5-windowsinstaller.exe
# 2)Install the program
# 3)Create inside kape\bin the folder "bulk_extractor" and copy the program "bulk_extractor.exe" from "C:\Program Files (x86)\Bulk Extractor 1.5.5\64-bit"
# Example KAPE CLI: .\kape.exe --msource D:\source --mdest D:\dest --mflush --module Bulk_extractor --gui
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
