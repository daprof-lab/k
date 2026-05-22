# 🎯 **Edge Chromium Extensions**
### `File Name: EdgeChromiumExtensions.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** cardinsou, Reece394  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Edge Chromium Extension Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Edge Chromium Extensions to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Edge Chromium Extensions events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Edge Chromium Extensions storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Edge Chromium Extension Files
Author: cardinsou, Reece394
Version: 1.1
Id: 20b17ef1-c9eb-4c16-b373-31e5af9bc066
RecreateDirectories: true
Targets:
    -
        Name: Edge Chromium Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge\User Data\*\Extensions\
        Recursive: true
    -
        Name: Edge Beta Chromium Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge Beta\User Data\*\Extensions\
        Recursive: true
    -
        Name: Edge Dev Chromium Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge Dev\User Data\*\Extensions\
        Recursive: true
    -
        Name: Edge SxS - Canary Chromium Extension Files
        Category: Communications
        Path: C:\Users\%user%\AppData\Local\Microsoft\Edge SxS\User Data\*\Extensions\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
