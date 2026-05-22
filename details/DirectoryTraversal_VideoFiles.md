# 🎯 **Directory Traversal Video Files**
### `File Name: DirectoryTraversal_VideoFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find video files covering a multitude of formats

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Video Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Video Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Video Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find video files covering a multitude of formats
Author: Andrew Rathbun
Version: 1.0
Id: 93c954d7-048b-4a30-a714-8ee31f079fb9
RecreateDirectories: true
Targets:
    -
        Name: Video files
        Category: Multimedia
        Path: C:\
        FileMask: regex:*.+\.(3g2|3gp|amv|asf|avi|drc|flv|f4v|f4p|f4a|f4b|gif|gifv|m4v|mkv|mov|qt|mp4|m4p|mpg|mpeg|m2v|mp2|mpe|mpv|mts|m2ts|ts|mxf|nsv|ogv|ogg|rm|rmvb|roq|svi|viv|vob|webm|wmv|yuv)
        Recursive: true
        Comment: Covers most (if not all) video file formats

# Documentation
# https://en.wikipedia.org/wiki/Video_file_format
# Please note, this Target only looks for file extensions. It does not check the file header of each file, so be wary of video files that were changed to a file extension not listed above, such as .pptx or .pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
