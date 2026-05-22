# 🎯 **Img Burn**
### `File Name: ImgBurn.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Chuck Whitson  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ImgBurn

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Img Burn to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Img Burn events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Img Burn storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ImgBurn
Author: Chuck Whitson
Version: 1.0
Id: c70e3466-0ef7-48cc-aa24-a142266ed96e
RecreateDirectories: true
Targets:
    -
        Name: ImgBurn - Application Log File
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\ImgBurn\Log Files\
        FileMask: ImgBurn.log
        Comment: "Contains the ImgBurn application log file."

# Documentation
# https://forum.imgburn.com/topic/14632-where-can-i-find-the-imgburn-log
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
