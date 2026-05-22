# 🎯 **Directory Traversal Word Documents**
### `File Name: DirectoryTraversal_WordDocuments.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find Word and Word alternative documents

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Word Documents to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Word Documents events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Word Documents storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find Word and Word alternative documents
Author: Andrew Rathbun
Version: 1.0
Id: 81940872-6efb-4465-af0d-a896758f6bf3
RecreateDirectories: true
Targets:
    -
        Name: Word and Word-like Documents
        Category: Documents
        Path: C:\
        FileMask: regex:*.+\.(doc|docx|docm|dotx|dotm|docb|dot|wbk|odt|fodt|rtf|wp*|tmd)
        Recursive: true
        Comment: Covers all document file formats for Word, OpenOffice, LibreOffice, Apache OpenOffice, WPS Office, SoftMaker Office, and more

# Documentation
# https://en.wikipedia.org/wiki/List_of_Microsoft_Office_filename_extensions
# https://en.wikipedia.org/wiki/OpenDocument
# https://en.wikipedia.org/wiki/WordPerfect#WordPerfect_Office
# https://en.wikipedia.org/wiki/TextMaker
# https://en.wikipedia.org/wiki/Apache_OpenOffice#File_formats
# https://en.wikipedia.org/wiki/WPS_Office#File_format
# https://en.wikipedia.org/wiki/OnlyOffice#Desktop_editors
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
