# 🎯 **Directory Traversal Audio Files**
### `File Name: DirectoryTraversal_AudioFiles.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find audio files covering a multitude of formats

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Directory Traversal Audio Files to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Directory Traversal Audio Files events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Directory Traversal Audio Files storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Find audio files covering a multitude of formats
Author: Andrew Rathbun
Version: 1.0
Id: 2be677d4-2edf-4ba5-b7c4-c90630527fa0
RecreateDirectories: true
Targets:
    -
        Name: Audio files
        Category: Multimedia
        Path: C:\
        FileMask: regex:*.+\.(3gp|aa|aac|act|aiff|alac|amr|ape|au|awb|dss|dvf|flac|gsm|iklax|ivs|m4a|m4b|m4p|mmf|mp3|mpc|msv|nmf|ogg|oga|mogg|opus|ra|rm|raw|rf64|sln|tta|voc|vox|wav|wma|wv|webm)
        Recursive: true
        Comment: Covers most (if not all) audio file formats

# Documentation
# https://en.wikipedia.org/wiki/Audio_file_format
# Please note, this Target only looks for file extensions. It does not check the file header of each file, so be wary of music files that were changed to a file extension not listed above, such as .pptx or .pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
