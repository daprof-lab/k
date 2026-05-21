# 🎯 **RecentFileCache**
### `File Name: RecentFileCache.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Precursor file to Amcache (RecentFileCache.bcf) on older versions of Windows. It records paths and filenames of recently run applications.

---

## 🔍 **Investigative Use-Cases**
* **Legacy Execution Recovery**: Reconstruct application execution logs on Windows 7 systems where Amcache is missing or disabled.
* **Staged Binary Auditing**: Verify execution pathways of temporary executables hosted in User profile temp directories.
* **Simple Timeline Chronology**: Map process execution order based on basic cached lists of running binaries.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RecentFileCache
Author: Eric Zimmerman
Version: 1.0
Id: 0d93d3fc-1b09-4894-b21f-dddc7f269934
RecreateDirectories: true
Targets:
    -
        Name: RecentFileCache
        Category: ApplicationCompatibility
        Path: C:\Windows\AppCompat\Programs\
        FileMask: RecentFileCache.bcf
    -
        Name: RecentFileCache
        Category: ApplicationCompatibility
        Path: C:\Windows.old\Windows\AppCompat\Programs\
        FileMask: RecentFileCache.bcf

# Documentation
# https://digital-forensics.sans.org/media/poster-windows-forensics-final.pdf
# http://journeyintoir.blogspot.com/2013/12/revealing-recentfilecachebcf-file.html
# https://www.youtube.com/watch?v=ZKlyu-HOvxY
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
