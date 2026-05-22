# 🎯 **VIPRE**
### `File Name: VIPRE.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
VIPRE Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from VIPRE to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate VIPRE events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit VIPRE storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: VIPRE Data
Author: Drew Ervin
Version: 1.0
Id: 8af4ffd8-264e-4c7d-aa28-8cc4f543b01d
RecreateDirectories: true
Targets:
    -
        Name: VIPRE Business Agent Logs
        Category: Antivirus
        Path: C:\ProgramData\VIPRE Business Agent\Logs\
        Recursive: true
    -
        Name: VIPRE Business User Logs (v7+)
        Category: Antivirus
        Path: C:\Users\%user%\AppData\Roaming\VIPRE Business\
        Recursive: true
    -
        Name: VIPRE Business User Logs (v5-v6)
        Category: Antivirus
        Path: C:\Users\%user%\AppData\Roaming\GFI Software\AntiMalware\Logs\
        Recursive: true
    -
        Name: VIPRE Business User Logs (up to v4)
        Category: Antivirus
        Path: C:\Users\%user%\AppData\Roaming\Sunbelt Software\AntiMalware\Logs\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
