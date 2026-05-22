# 🎯 **Combofix**
### `File Name: Combofix.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ComboFix Antivirus Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Combofix to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Combofix events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Combofix storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ComboFix Antivirus Data
Author: Drew Ervin
Version: 1.0
Id: 8fb8608e-65ab-4fd1-b7a4-13618caf5ad7
RecreateDirectories: true
Targets:
    -
        Name: ComboFix
        Category: Antivirus
        Path: C:\
        FileMask: ComboFix.txt

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
