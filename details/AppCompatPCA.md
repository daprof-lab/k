# 🎯 **App Compat PCA**
### `File Name: AppCompatPCA.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
AppCompat PCA Folder

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from App Compat PCA to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate App Compat PCA events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit App Compat PCA storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: AppCompat PCA Folder
Author: Andrew Rathbun
Version: 1.0
Id: fa6b3393-1bb9-4c2a-aa35-fa138d2d090a
RecreateDirectories: true
Targets:
    -
        Name: AppCompat PCA Folder
        Category: ApplicationCompatibility
        Path: C:\Windows\appcompat\pca

# Documentation
# https://aboutdfir.com/new-windows-11-pro-22h2-evidence-of-execution-artifact/
# https://blog.sygnia.co/diving-into-the-new-windows-11-pca-artifact
# Credit to rancio#4162 on the Digital Forensics Discord Server who noticed this artifact - https://discord.com/channels/427876741990711298/427936091220344833/1057680326484299786
# This artifact appears to be on Windows 11 only and will comprise of the following files:
# C:\Windows\appcompat\pca\PcaAppLaunchDic.txt
# C:\Windows\appcompat\pca\PcaGeneralDb1.txt
# C:\Windows\appcompat\pca\PcaGeneralDb0.txt
# PcaAppLaunchDic.txt appears to contain reliable timestamps for evidence of last execution in the format of FILE PATH | TIMESTAMP
# I've tested and validated this on my own Windows 11 Pro system where the timestamps updates in real-time upon execution of a given application
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
