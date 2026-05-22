# 🎯 **Directory Traversal Pdfdocuments**
### `File Name: DirectoryTraversal_PDFDocuments.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find PDF and PDF alternative documents

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Pdfdocuments to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Pdfdocuments events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Pdfdocuments storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find PDF and PDF alternative documents
Author: Andrew Rathbun
Version: 1.0
Id: 1bd73cdb-8220-426c-bd91-0d0554f0c8bc
RecreateDirectories: true
Targets:
    -
        Name: PDF and PDF-like Documents
        Category: Documents
        Path: C:\
        FileMask: regex:*.+\.(pdf|xps|oxps)
        Recursive: true
        Comment: Covers all PDF and PDF-like document formats

# Documentation
# https://www.prepressure.com/pdf/basics/versus-other-formats
# https://en.wikipedia.org/wiki/PDF#Alternatives
# https://en.wikipedia.org/wiki/Open_XML_Paper_Specification
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
