# 🎯 **Edge**
### `File Name: Edge.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Edge

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Edge to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Edge events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Edge storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Edge
Author: Phill Moore
Version: 1.0
Id: c72bd45c-2a24-4df9-aa0b-3d7048c90337
RecreateDirectories: true
Targets:
    -
        Name: Edge folder
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\
        Recursive: true

# Documentation
# https://www.forensafe.com/blogs/microsoftedge.html
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
