# 🎯 **Hitman Pro**
### `File Name: HitmanPro.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
HitmanPro Antivirus Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Hitman Pro to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Hitman Pro events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Hitman Pro storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: HitmanPro Antivirus Data
Author: Drew Ervin
Version: 1.0
Id: db98e01b-bd07-4b40-a6ef-e75bdef39bb2
RecreateDirectories: true
Targets:
    -
        Name: HitmanPro Logs
        Category: Antivirus
        Path: C:\ProgramData\HitmanPro\Logs\
        Recursive: true
    -
        Name: HitmanPro Alert Logs
        Category: Antivirus
        Path: C:\ProgramData\HitmanPro.Alert\Logs\
        Recursive: true
    -
        Name: HitmanPro Database
        Category: Antivirus
        Path: C:\ProgramData\HitmanPro.Alert\
        FileMask: excalibur.db
        Comment: "SQLite DB"
    -
        Name: HitmanPro Quarantine
        Category: Antivirus
        Path: C:\ProgramData\HitmanPro\Quarantine
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
