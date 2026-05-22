# 🎯 **Whats App Media**
### `File Name: WhatsApp_Media.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** SolitudePy  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WhatsApp Shared Media Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Whats App Media to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Whats App Media events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Whats App Media storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: WhatsApp Shared Media Files
Author: SolitudePy
Version: 1.0
Id: b148236d-1064-42c4-bbb2-f08ad7aa8530
RecreateDirectories: true
Targets:
    -
        Name: Microsoft Store WhatsApp Desktop Profile Pictures
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Packages\*WhatsAppDesktop*\LocalState\profilePictures
        Comment: "Copies the local store of contacts profile pictures, simply open with a photos software"
    -
        Name: Microsoft Store WhatsApp Shared Media
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Packages\*WhatsAppDesktop*\LocalState\shared\transfers
        Recursive: true
        FileMask: regex:.*\.(jpg|mp4|pdf|webp)
        Comment: "Copies the shared media, can get very large."


# Documentation
# Whatsapp Desktop saves shared media locally, simply open it with a media software.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
