# 🎯 **Windows Network**
### `File Name: WindowsNetwork.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Zawadi Done  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Networks settings

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Network to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Network events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Network storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Windows Networks settings
Author: Zawadi Done
Version: 1.0
Id: aeacb435-8929-4414-b1ee-24d4f7273ea5
RecreateDirectories: true
Targets:
    -
        Name: Network setting files
        Category: Misc
        Path: C:\windows\system32\drivers\etc
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
