# 🎯 **Directory Traversal Excel Documents**
### `File Name: DirectoryTraversal_ExcelDocuments.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find Excel and Excel alternative documents

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Excel Documents to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Excel Documents events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Excel Documents storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find Excel and Excel alternative documents
Author: Andrew Rathbun
Version: 1.0
Id: 010e7a3b-2c62-4d6c-8fa0-34cdc6e32524
RecreateDirectories: true
Targets:
    -
        Name: Excel and Excel-like Documents
        Category: Documents
        Path: C:\
        FileMask: regex:*.+\.(xls|xlsx|csv|tsv|xlt|xlm|xlsm|xltx|xltm|xlsb|xla|xlam|xll|xlw|ods|fodp|qpw)
        Recursive: true
        Comment: Covers all document file formats for Excel, OpenOffice, LibreOffice, Apache OpenOffice, WPS Office, SoftMaker Office, and more

# Documentation
# https://en.wikipedia.org/wiki/List_of_Microsoft_Office_filename_extensions
# https://en.wikipedia.org/wiki/Comparison_of_spreadsheet_software
# https://en.wikipedia.org/wiki/OpenDocument
# https://en.wikipedia.org/wiki/WordPerfect#WordPerfect_Office
# https://en.wikipedia.org/wiki/PlanMaker
# https://en.wikipedia.org/wiki/Apache_OpenOffice#File_formats
# https://en.wikipedia.org/wiki/WPS_Office#File_format
# https://en.wikipedia.org/wiki/OnlyOffice#Desktop_editors
# https://en.wikipedia.org/wiki/Quattro_Pro#Characteristics
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
