# 🎯 **Q Dir**
### `File Name: Q-Dir.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Q-Dir

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Q Dir to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Q Dir events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Q Dir storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Q-Dir
Author: Andrew Rathbun
Version: 1.0
Id: 1233adac-a6ec-4bba-abe6-c827ba5e27ea
RecreateDirectories: true
Targets:
    -
        Name: Q-Dir - .ini File
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Q-Dir\
        FileMask: 'Q-Dir.ini'
        Comment: "Locates .ini file associated with Q-Dir which stores useful user activity information."
    -
        Name: Q-Dir - .qdr file
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Q-Dir\
        FileMask: 'start.qdr'
        Comment: "Locates .qdr file associated with Q-Dir which stores useful user activity information, including the last 4 folders opened (encoded, unfortunately)."

# Documentation
# Q-Dir is a freeware Windows File Explorer replacement similar to Total Commander and other orthodox file managers.
# Q-Dir has limited FTP functionality as of April 2021.
# The .ini is not the most helpful. It appears everything is stored in a currently unknown encoding format.
# Same story for start.qdr. However, this is where all the info the program stores at this time resides.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
