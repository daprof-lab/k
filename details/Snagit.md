# 🎯 **Snagit**
### `File Name: Snagit.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Snagit

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Snagit to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Snagit events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Snagit storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Snagit
Author: Andrew Rathbun
Version: 1.0
Id: b2281102-476c-4aa2-804d-4c906a20415a
RecreateDirectories: true
Targets:
    -
        Name: Snagit - Captures
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\TechSmith\Snagit\DataStore
        Comment: "Locates all Snagit captures"

# Documentation
# Snagit is an awesome, premium screen capturing software that is totally worth looking into.
# Captures with Snagit are stored as .SNAG files, which can be opened with Snagit Editor.
# Think of Snagit as Snipping Tool on steroids. The user can create robust diagrams and guides on top of the captured image.
# This target will grab all the contents of the DataStore folder.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
