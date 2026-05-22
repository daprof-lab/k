# 🎯 **Fast Stone Image Viewer**
### `File Name: FastStoneImageViewer.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
FastStone Image Viewer

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Fast Stone Image Viewer to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Fast Stone Image Viewer events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Fast Stone Image Viewer storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: FastStone Image Viewer
Author: DReneau
Version: 1.0
Id: 77acde9a-fbb5-4d2b-8ebf-191ad5fc7f55
RecreateDirectories: true
Targets:
    -
        Name: FastStone Image Viewer (FSIV)
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\FastStone\FSIV\
        FileMask: 'FSIV.db'
        Comment: Image browser, converter, and editor that supports all major graphic formats.

# Documentation
# https://www.faststone.org/index.htm
# FSIV.db is the FastStone's primary database for stored metadata.
# https://en.wikipedia.org/wiki/FastStone_Image_Viewer
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
