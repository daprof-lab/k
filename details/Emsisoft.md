# 🎯 **Emsisoft**
### `File Name: Emsisoft.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** blueskycyber  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Emsisoft Antivirus Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Emsisoft to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Emsisoft events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Emsisoft storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Emsisoft Antivirus Logs
Author: blueskycyber
Version: 1.0
Id: f810ea6e-eb10-4788-bff7-77bd83fe15d2
RecreateDirectories: true
Targets:
    -
        Name: Emsisoft Scan Logs
        Category: ApplicationLogs
        Path: C:\ProgramData\Emsisoft\Reports\
        FileMask: scan*.txt
        Comment: "Can contain file detection and quarantine info"
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
