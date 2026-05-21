# 🎯 **MegaSync Client**
### `File Name: Megasync.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MegaSync synchronization metadata, active downloads list, and connected user accounts.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from MegaSync Client to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate MegaSync Client events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit MegaSync Client storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MegaSync Data Collection
Author: Vito Alfano
Version: 1.0
Id: a6c7f66e-b37c-4895-98c3-4eb9775623cf
RecreateDirectories: true
Targets:
    -
        Name: MegaSync Folder
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Local\Mega Limited\MEGAsync\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
