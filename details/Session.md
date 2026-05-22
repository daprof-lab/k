# 🎯 **Session**
### `File Name: Session.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Session Desktop

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Session to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Session events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Session storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Session Desktop
Author: Vito Alfano
Version: 1.0
Id: c6633dbf-caea-48dc-90a0-25add823134d
RecreateDirectories: true
Targets:
    -
        Name: Session App Folder
        Category: Apps
        Path: C:\Users\%user%\AppData\Roaming\Session\
        Recursive: true
        Comment: "Session App Folder"

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
