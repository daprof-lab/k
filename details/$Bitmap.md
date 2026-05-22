# 🎯 **$bitmap**
### `File Name: $Bitmap.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Nisarg Suthar  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
$Bitmap

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from $bitmap to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate $bitmap events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit $bitmap storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $Bitmap
Author: Nisarg Suthar
Version: 1.0
Id: 53303f6f-a8ee-47c3-8468-90cf01501215
RecreateDirectories: true
Targets:
    -
        Name: $Bitmap
        Category: FileSystem
        Path: C:\
        FileMask: $Bitmap
        AlwaysAddToQueue: true

# Documentation
# https://whereismydata.wordpress.com/2009/06/01/forensics-what-is-the-bitmap/
# https://flatcap.github.io/linux-ntfs/ntfs/files/bitmap.html
# https://kcall.co.uk/ntfs/
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
