# 🎯 **Explorer Thumbnail Cache**
### `File Name: ThumbCache.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System-generated cached databases (thumbcache_*.db) storing visual previews of pictures, videos, documents, and folders rendered in Windows Explorer.

---

## 🔍 **Investigative Use-Cases**
* **Deleted Visual Evidence Recovery**: Recover thumbnail images of deleted evidence, documents, or photos that are no longer present on disk.
* **Contraband Identification**: Find visual traces of illicit media files, sensitive spreadsheets, or design documents.
* **System Familiarity Auditing**: Prove that a directory containing custom images was visually browsed by a user.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Thumbcache DB
Author: Eric Zimmerman
Version: 1.0
Id: 1eec8849-b6eb-475b-a700-f4fb0055356d
RecreateDirectories: true
Targets:
    -
        Name: Thumbcache DB
        Category: FileKnowledge
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\Explorer\
        FileMask: 'thumbcache_*.db'

# Documentation
# https://digitalforensicsurvivalpodcast.com/2017/04/04/dfsp-059-thumbcache-forensics/
# https://papers.ssrn.com/sol3/Delivery.cfm/SSRN_ID2429795_code2138273.pdf?abstractid=2429795&mirid=1
# https://people.cs.umass.edu/~liberato/courses/2019-spring-compsci365/lecture-notes/18-more-windows-forensics/
# https://www.researchgate.net/publication/273461120_Forensic_Analysis_of_Windows_Thumbcache_Files
# https://www.forensafe.com/blogs/thumbcache.html
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
