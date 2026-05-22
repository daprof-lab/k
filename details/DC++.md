# 🎯 **DC++**
### `File Name: DC++.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
DC++

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from DC++ to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate DC++ events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit DC++ storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: DC++
Author: Andrew Rathbun
Version: 1.0
Id: 577569f8-e10f-4513-9c59-19d17a10eccb
RecreateDirectories: true
Targets:
    -
        Name: DC++ Chat Logs
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\DC++\Logs\
        Recursive: true
        Comment: "Locates DC++ hub/chat logs and copies them. Current as of version 0.868."

# Documentation
# DC++ is a popular file-sharing client that runs on the Direct Connect network.
# DC++ is commonly used to share any file type with any users either directly or within chat rooms (hubs).
# Hub/chat logs are plain text readable with your favorite text editor.
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
