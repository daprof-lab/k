# 🎯 **Signature Catalog**
### `File Name: SignatureCatalog.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mike Pilkington  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Obtain detached signature catalog files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Signature Catalog to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Signature Catalog events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Signature Catalog storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Obtain detached signature catalog files
Author: Mike Pilkington
Version: 1.0
Id: 953b16e8-69ea-4967-9f9b-bcfa4f4fbe7b
RecreateDirectories: true
Targets:
    -
        Name: SignatureCatalog
        Category: FileMetadata
        Path: C:\Windows\System32\CatRoot\
        Recursive: true
    -
        Name: SignatureCatalog
        Category: FileMetadata
        Path: C:\Windows.old\Windows\System32\CatRoot\
        Recursive: true

# Documentation
# Validating digital signatures of an offline system can be problematic.
# Microsoft relies mostly on detached signature files to sign Windows
# executables.  Checking those on an offline system using sigcheck.exe
# from SysInternals requires importing the target system's detached
# signature files into the anlysis system.  To use with sigcheck, slightly
# rename the collected GUID directories (keeping the names in a GUID format),
# copy them to C:\Windows\System32\CatRoot of your analysis machine, restart
# Cryptographic Services, then run sigcheck against the target system files.
# This will import the target's signature files into the local analysis
# machine's signature database and should accurately validate the target
# system's files (which presumabley were collected with other KAPE modules).
# Kudos to Troy Larson for providing this workaround technique.
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
