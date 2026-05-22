# 🎯 **Tree Size**
### `File Name: TreeSize.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
TreeSize - Scan History

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Tree Size to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Tree Size events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Tree Size storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: TreeSize - Scan History
Author: Andrew Rathbun
Version: 1.0
Id: b7e88f6b-3474-46b1-9c0b-1eed65dfc379
RecreateDirectories: true
Targets:
    -
        Name: TreeSize - ScanHistory.XML
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\JAM Software\TreeSize
        FileMask: 'scanhistory.xml'
        Comment: "Locates XML file that provides a list of previously scanned directories by the user."

# Documentation
# https://www.jam-software.com/treesize_free
# TreeSize is a program similar to WinDirStat which allows the user to enumerate their computer's file system in a variety of ways
# ScanHistory.XML will provide listings that look similar to this
# <SCANS>
# 	<Root path="\\HOSTNAME\C$\">
# 		<Path>\\HOSTNAME\C$\</Path>
# 		<Date>44148.3234845949</Date>
# 		<Version>8.0.2.1505</Version>
# 		<SizeData Size="210610089818" Allocated="187592699904" Files="678331"/>
# 		<Freespace>814266826752</Freespace>
# 	</Root>
# For each scan ran, there will be an entry in this file
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
