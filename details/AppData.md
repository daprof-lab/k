# 🎯 **App Data**
### `File Name: AppData.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
AppData

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from App Data to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate App Data events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit App Data storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: AppData
Author: Phill Moore
Version: 1.1
Id: f8314fc9-3c07-48e9-bb10-539c0dc39ea7
RecreateDirectories: true
Targets:
    -
        Name: AppData
        Category: UserData
        Path: C:\Users\%user%\AppData\
        Recursive: true

# Documentation:
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
