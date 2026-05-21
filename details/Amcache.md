# 🎯 **Amcache Database**
### `File Name: Amcache.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
System database hive (Amcache.hve) logging metadata of newly installed applications, executable file paths, compiler compilation times, and SHA-1 file hashes.

---

## 🔍 **Investigative Use-Cases**
* **Unsigned Binary Auditing**: Extract SHA-1 file hashes of executed binaries to run threat-intelligence queries on platforms like VirusTotal.
* **Application Install Timeline**: Establish installation timelines and executable directories for newly staged backdoors or software packages.
* **Compilation Anomaly Detection**: Identify timestomping attempts by comparing compiler timestamps against file-creation times.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Amcache.hve
Author: Eric Zimmerman
Version: 1.0
Id: 13ba1e33-4899-4843-adf1-c7e6b20d759a
RecreateDirectories: true
Targets:
    -
        Name: Amcache
        Category: ApplicationCompatibility
        Path: C:\Windows\AppCompat\Programs\
        FileMask: Amcache.hve
    -
        Name: Amcache
        Category: ApplicationCompatibility
        Path: C:\Windows.old\Windows\AppCompat\Programs\
        FileMask: Amcache.hve
    -
        Name: Amcache transaction files
        Category: ApplicationCompatibility
        Path: C:\Windows\AppCompat\Programs\
        FileMask: Amcache.hve.LOG*
    -
        Name: Amcache transaction files
        Category: ApplicationCompatibility
        Path: C:\Windows.old\Windows\AppCompat\Programs\
        FileMask: Amcache.hve.LOG*

# Documentation
# https://digital-forensics.sans.org/media/poster-windows-forensics-final.pdf
# https://www.youtube.com/watch?v=_DqTBYeQ8yA
# https://www.youtube.com/watch?v=-0bYcD3_bBs
# https://www.youtube.com/watch?v=iTchBtRr6TA
# https://www.andreafortuna.org/2017/10/16/amcache-and-shimcache-in-forensic-analysis/
# https://www.forensafe.com/blogs/amcache.html
# https://commons.erau.edu/cgi/viewcontent.cgi?article=1429&context=jdfsl
# https://www.thedfirspot.com/post/evidence-of-program-existence-amcache
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
