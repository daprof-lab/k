# 🎯 **Directory Traversal Picture Files**
### `File Name: DirectoryTraversal_PictureFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find picture files covering a multitude of formats

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Picture Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Picture Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Picture Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find picture files covering a multitude of formats
Author: Andrew Rathbun
Version: 1.0
Id: 1875e15e-3a3e-4468-8b3e-a3a240b4c470
RecreateDirectories: true
Targets:
    -
        Name: Picture files
        Category: Multimedia
        Path: C:\
        FileMask: regex:*.+\.(ai|bmp|bpg|cdr|cpc|eps|exr|flif|gif|heif|ilbm|ima|jp2|j2k|jpf|jpm|jpg2|j2c|jpc|jpx|mj2jpeg|jpg|jxl|kra|ora|pcx|pgf|pgm|png|pnm|ppm|psb|psd|psp|svg|tga|tiff|webp|xaml|xcf)
        Recursive: true
        Comment: Covers most (if not all) picture file formats

# Documentation
# https://en.wikipedia.org/wiki/Image_file_formats
# Please note, this Target only looks for file extensions. It does not check the file header of each file, so be wary of picture files that were changed to a file extension not listed above, such as .pptx or .pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
