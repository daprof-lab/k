# 🎯 **Syncthing**
### `File Name: Syncthing.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Syncthing Configuration and Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Syncthing to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Syncthing events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Syncthing storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Syncthing Configuration and Logs
Author: Vito Alfano
Version: 1.0
Id: 2ff816bf-c087-48ef-bed4-a148178f51e2
RecreateDirectories: true
Targets:
    -
        Name: Syncthing Configuration and Certificates
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\Syncthing\
        Comment: "Folder storing Syncthing configuration and certificates"
    -
        Name: Syncthing Cache and Storage
        Category: Apps
        Path: C:\Users\%user%\AppData\Local\SyncTrazor\
        Comment: "Folder storing session and storage cache"
    -
        Name: Syncthing Logs
        Category: ApplicationLogs
        Path: C:\Users\%user%\AppData\Roaming\SyncTrazor\
        Comment: "Folder storing Syncthing session logs"

# Documentation
# https://syncthing.net/
# https://docs.syncthing.net/
# https://www.bleepingcomputer.com/news/security/ukraine-says-hackers-abuse-syncthing-tool-to-steal-data/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
