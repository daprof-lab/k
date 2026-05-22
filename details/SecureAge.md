# 🎯 **Secure Age**
### `File Name: SecureAge.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SecureAge Antivirus Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Secure Age to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Secure Age events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Secure Age storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SecureAge Antivirus Logs
Author: Andrew Rathbun
Version: 1.0
Id: 3876be71-fd3d-4455-bb70-80541370f2a0
RecreateDirectories: true
Targets:
    -
        Name: SecureAge Antvirus Logs
        Category: Antivirus
        Path: C:\ProgramData\SecureAge Technology\SecureAge\log\
        Recursive: true

# Documentation
# This Target should pull the following log files:
# Antivirus.log - will have a list of files that were scanned. Good for locating files as they appear on the file system that may no longer exist
# clamd.log
# SecureAPlus.log
# UniversalAV.log
# whitelist.log
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
