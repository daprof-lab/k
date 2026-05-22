# 🎯 **$SDS**
### `File Name: $SDS.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman and Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
$SDS

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from $SDS to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate $SDS events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit $SDS storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $SDS
Author: Eric Zimmerman and Andrew Rathbun
Version: 1.1
Id: 72d56db2-b8da-4830-a2e7-37437c90e18f
RecreateDirectories: true
Targets:
    -
        Name: $SDS
        Category: FileSystem
        Path: C:\
        FileMask: $Secure:$SDS
        AlwaysAddToQueue: true
        SaveAsFileName: $Secure_$SDS
    -
        Name: $SDS
        Category: FileSystem
        Path: C:\
        FileMask: $Secure_$SDS
        SaveAsFileName: $Secure_$SDS
        Comment: "This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Target is looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed"

# Documentation
# https://digital-forensics.sans.org/media/DFIR-Command-Line.pdf
# https://www.youtube.com/watch?v=ZCj7cbWwUOs
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
