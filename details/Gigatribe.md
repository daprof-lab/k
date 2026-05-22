# 🎯 **Gigatribe**
### `File Name: Gigatribe.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Linus Nissi  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gigatribe Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Gigatribe to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Gigatribe events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Gigatribe storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Gigatribe Files
Author: Linus Nissi
Version: 2.0
Id: 64726d74-1a68-463a-bb26-929054a20b71
RecreateDirectories: true
Targets:
    -
        Name: Gigatribe Files Windows Vista/7/8/10
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Shalsoft\
        Recursive: true
        Comment: "Locates Gigatribe files and copies them"
    -
        Name: Gigatribe Files Windows XP
        Category: FileDownload
        Path: C:\Documents and Settings\%user%\*\Application Data\Gigatribe\
        Recursive: true
        Comment: Locates Gigatribe files and copies them. Different path depending on the Operating System language. In Swedish the location is C:\Documents and Settings\<username>\Lokala Inställningar\Application Data\Gigatribe
    -
        Name: Gigatribe Files Windows XP
        Category: FileDownload
        Path: C:\Documents and Settings\%user%\*\Application Data\Shalsoft\
        Recursive: true
        Comment: Locates Gigatribe files and copies them. Different path depending on the Operating System language. In Swedish the location is C:\Documents and Settings\<username>\Lokala Inställningar\Application Data\Shalsoft

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
