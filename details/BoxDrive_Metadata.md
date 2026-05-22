# 🎯 **Box Drive Metadata**
### `File Name: BoxDrive_Metadata.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Chad Tilbury  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Box Cloud Storage Metadata

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Box Drive Metadata to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Box Drive Metadata events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Box Drive Metadata storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Box Cloud Storage Metadata
Author: Chad Tilbury
Version: 1.1
Id: 00d36d65-dbbc-45f5-801e-c78efb3dfcfa
RecreateDirectories: true
Targets:
    -
        Name: Box Drive Application Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Box\Box\
        Recursive: true
    -
        Name: Box Sync Application Metadata
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Box Sync\
        Recursive: true

# Documentation
# https://cyberforensicator.com/2018/04/21/cloud-forensics-box/
# https://dpmforensics.com/2017/03/12/cloud-forensics-box/
# https://www.sans.org/blog/cloud-storage-acquisition-from-endpoint-devices
# https://www.researchgate.net/publication/340816615_Forensic_Analysis_in_Cloud_Storage_with_Live_Forensics_in_Windows_Adrive_Case_Study
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
