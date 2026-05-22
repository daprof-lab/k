# 🎯 **Superanti Spyware**
### `File Name: SUPERAntiSpyware.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SUPERAntiSpyware Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Superanti Spyware to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Superanti Spyware events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Superanti Spyware storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SUPERAntiSpyware Data
Author: Drew Ervin
Version: 1.0
Id: 0b2c9e30-8d85-43ea-aa26-b20503b8e1da
RecreateDirectories: true
Targets:
    -
        Name: SUPERAntiSpyware Logs
        Category: Antivirus
        Path: C:\Users\%user%\AppData\Roaming\SUPERAntiSpyware\Logs\
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
