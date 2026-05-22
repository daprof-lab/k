# 🎯 **$mftmirr**
### `File Name: $MFTMirr.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Teo Kia Meng  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
$MFTMirr

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from $mftmirr to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate $mftmirr events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit $mftmirr storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: $MFTMirr
Author: Teo Kia Meng
Version: 1.0
Id: 8fce369c-a773-41c4-8ca3-ba9df1f72ba0
RecreateDirectories: true
Targets:
    -
        Name: $MFTMirr
        Category: FileSystem
        Path: C:\
        FileMask: $MFTMirr
        AlwaysAddToQueue: true
        Comment: "$MFTMirr is a redundant copy of the first four (4) records of the MFT."

# Documentation
# $MFTMirr is a redundant copy of the first four (4) records of the MFT.
# https://flatcap.org/linux-ntfs/ntfs/files/mftmirr.html
# https://digital-forensics.sans.org/media/DFIR-Command-Line.pdf
# https://www.andreafortuna.org/2017/10/06/macb-times-in-windows-forensic-analysis/
# https://www.andreafortuna.org/2018/06/04/using-mft-anomalies-to-spot-suspicious-files-in-forensic-analysis/
# https://www.thedigitalforensics.com/windows-forensics/timestamp-in-ntfs-system
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
