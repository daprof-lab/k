# 🎯 **Freenet**
### `File Name: Freenet.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Charlie Rubisoff  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Freenet

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Freenet to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Freenet events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Freenet storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Freenet
Author: Charlie Rubisoff
Version: 1.0
Id: dbf16082-0a99-4d3e-b24d-5fb20a1bd914
RecreateDirectories: true
Targets:
    -
        Name: Freenet
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Freenet\
        FileMask: 'node*'
    -
        Name: Freenet
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Freenet\
        FileMask: '*completed.list.downloads'
    -
        Name: Freenet
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Freenet\
        FileMask: '*completed.list.uploads'
    -
        Name: Freenet
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Freenet\
        FileMask: '*.bak'
    -
        Name: Freenet
        Category: FileDownload
        Path: C:\Users\%user%\AppData\Local\Freenet\downloads\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
