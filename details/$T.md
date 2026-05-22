# 🎯 **$T**
### `File Name: $T.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman and Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
$T

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from $T to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate $T events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit $T storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $T
Author: Eric Zimmerman and Andrew Rathbun
Version: 1.1
Id: 8c568aa0-9a67-4035-9720-1423770bc29a
RecreateDirectories: true
Targets:
    -
        Name: $T
        Category: FileSystem
        Path: C:\$Extend\$RmMetadata\$TxfLog\
        FileMask: $Tops:$T
        AlwaysAddToQueue: true
        SaveAsFileName: $T
    -
        Name: $T
        Category: FileSystem
        Path: C:\$Extend\$RmMetadata\$TxfLog\
        FileMask: $T
        SaveAsFileName: $T
        Comment: "This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Target is looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed"

# Documentation
# TxF Old Page Stream (TOPS) file Used to store data that has been overwritten inside a currently active transaction
# https://github.com/libyal/libfsntfs/blob/main/documentation/New%20Technologies%20File%20System%20(NTFS).asciidoc#17-transactional-ntfs-txf
# https://forensicswiki.xyz/wiki/index.php?title=New_Technology_File_System_(NTFS)#Transactional_NTFS_.28TxF.29
# https://web.archive.org/web/20080830093028/http://msdn.microsoft.com/en-us/magazine/cc163388.aspx
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
