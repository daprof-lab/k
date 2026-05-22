# 🎯 **Rogue Killer**
### `File Name: RogueKiller.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RogueKiller Anti-Malware (by Adlice Software)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Rogue Killer to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Rogue Killer events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Rogue Killer storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: RogueKiller Anti-Malware (by Adlice Software)
Author: Drew Ervin
Version: 1.0
Id: 089b2afb-cc29-4565-9c2f-cbf0ba50f10d
RecreateDirectories: true
Targets:
    -
        Name: RogueKiller Reports
        Category: Antivirus
        Path: C:\ProgramData\RogueKiller\logs\
        FileMask: AdliceReport_*.json

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
