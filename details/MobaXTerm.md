# 🎯 **Moba Xterm**
### `File Name: MobaXTerm.tkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MobaXTerm

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Moba Xterm to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Moba Xterm events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Moba Xterm storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MobaXTerm
Author: Andrew Rathbun
Version: 1.0
Id: 5c219ccc-1415-4bf1-9e76-da0a9e91983c
RecreateDirectories: true
Targets:
    -
        Name: MobaXTerm Logs
        Category: Communications
        Path: C:\Users\%user%\AppData\Roaming\MobaXterm
        Recursive: true
        Comment: Contains what appears to be a Linux Filesystem that's set up upon use of MobaXTerm

# Documentation
# https://mobaxterm.mobatek.net/
```
---

[⬅️ Back to Cloud Storage & Remote Access Targets](../cloud_remote_targets.md)
