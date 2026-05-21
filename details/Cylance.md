# 🎯 **Cylance Antivirus**
### `File Name: Cylance.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Ron Rader  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Local threat telemetry logs, configuration profiles, and scan logs from Cylance Protect.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cylance Antivirus to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cylance Antivirus events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cylance Antivirus storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Cylance Antivirus Logs
Author: Ron Rader
Version: 1.0
Id: 83411cbd-a6b2-4a9e-90e0-eec9bcd160a3
RecreateDirectories: true
Targets:
    -
        Name: Cylance ProgramData Logs
        Category: Antivirus
        Path: C:\ProgramData\Cylance\Desktop
        Recursive: true
    -
        Name: Cylance Optics Logs
        Category: Antivirus
        Path: C:\ProgramData\Cylance\Optics\Log
        Recursive: true
    -
        Name: Cylance Program Files Logs
        Category: Antivirus
        Path: C:\Program Files\Cylance\Desktop\log
        Recursive: true

# Documentation
# Use SQLECmd to process the chp.db log
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
