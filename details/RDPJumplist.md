# 🎯 **Rdpjumplist**
### `File Name: RDPJumplist.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Vito Alfano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RDP Jumplist Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Rdpjumplist to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Rdpjumplist events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Rdpjumplist storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RDP Jumplist Files
Author: Vito Alfano
Version: 1.0
Id: da62b852-7af2-4882-ac83-ff3e142da2ef
RecreateDirectories: true
Targets:
    -
        Name: RDP Jumplist Files
        Category: FileSystem
        Path: C:\Users\%user%\AppData\Local\Packages\Microsoft.RemoteDesktop_8wekyb3d8bbwe\
        Recursive: true

# Documentation
# https://www.zerofox.com/blog/remote-desktop-application-vs-mstsc-forensics-the-rdp-artifacts-you-might-be-missing/
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
