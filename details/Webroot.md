# 🎯 **Webroot**
### `File Name: Webroot.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Webroot Antivirus

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Webroot to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Webroot events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Webroot storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Webroot Antivirus
Author: Drew Ervin
Version: 1.0
Id: c53c2b4e-075b-4162-b93e-aaf8c968e0b0
RecreateDirectories: true
Targets:

    -
        Name: Webroot Program Data
        Category: Antivirus
        Path: C:\ProgramData\WRData\
        FileMask: WRLog.log

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
