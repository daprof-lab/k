# 🎯 **Xprestore Points**
### `File Name: XPRestorePoints.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
XP Restore Points - System Volume Information directory

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Xprestore Points to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Xprestore Points events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Xprestore Points storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: XP Restore Points - System Volume Information directory
Author: Phill Moore
Version: 1.0
Id: 07f57a75-f9d9-42f3-842c-bd7e5abbb569
RecreateDirectories: true
Targets:
    -
        Name: System Volume Information
        Category: Folder capture
        Path: C:\System Volume Information\
        Recursive: true

# Documentation
# https://www.sans.org/security-resources/posters/windows-forensic-analysis/170/download
# https://topic.alibabacloud.com/a/font-classtopic-s-color00c1derestorefont-point-forensics-notes-for-the-forensic-processing-of-windows-xp-font-classtopic-s-color00c1derestorefont-points_1_15_32116346.html
# https://www.researchgate.net/publication/220345974_Forensic_analysis_of_System_Restore_points_in_Microsoft_Windows_XP
# https://www.stevebunting.org/udpd4n6/forensics/restorepoints.htm
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
