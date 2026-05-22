# 🎯 **M Remote NG**
### `File Name: mRemoteNG.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Markus Einarsson (@einarssonm)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
mRemoteNG

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from M Remote NG to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate M Remote NG events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit M Remote NG storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: mRemoteNG
Author: Markus Einarsson (@einarssonm)
Version: 1.0
Id: 486c2b29-ae39-4418-8fb4-2d855e9387f9
RecreateDirectories: true
Targets:
    -
        Name: mRemoteNG Logs
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\mRemoteNG\
        FileMask: mRemoteNG.log
        Comment: Contains log entries for remote connections
    -
        Name: mRemoteNG Connection Configuration and Backups
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\mRemoteNG\
        FileMask: confCons.xml*
        Comment: Contains connection config, often with obfuscated credentials
    -
        Name: mRemoteNG Program Settings
        Category: Communications
        Path: C:\Users\%user%\AppData\*\mRemoteNG\
        Recursive: true
        FileMask: user.config
        Comment: Contains user-specific program settings

# Documentation
# https://mremoteng.org/
# https://vk9-sec.com/exploiting-mremoteng/
# mRemoteNG is an open source, multi-protocol, remote connections manager for Windows.
# It handles connections for RDP, VNC, SSH, Telnet, rlogin and other protocols.
# The stored credentials are encrypted with a static key and base64 encoded.
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
