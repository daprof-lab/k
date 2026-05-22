# 🎯 **Fences**
### `File Name: Fences.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Fences

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Fences to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Fences events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Fences storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Fences
Author: Andrew Rathbun
Version: 1.0
Id: fbfd4a5b-130c-437b-b896-769813fd23e1
RecreateDirectories: true
Targets:
    -
        Name: Fences - Desktop Screenshots
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Stardock\Fences\Backups
        Comment: "Locates all screenshots taken automatically by the Fences application"

# Documentation
# Fences is a great application for helping to organizes your desktop. It's very similar to Nimi Places.
# Fences takes a daily snapshot of the user's desktop.
# Fences also takes a PreInstallSnapshot and OnInstallSnapshot that can potentially be useful for the historical contents of a user's desktop.
# Please note, if the user has multiple monitors, it will grab the contents of all monitors into one .PNG file.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
