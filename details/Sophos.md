# 🎯 **Sophos**
### `File Name: Sophos.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin, Reece394  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Sophos Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Sophos to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Sophos events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Sophos storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Sophos Data
Author: Drew Ervin, Reece394
Version: 1.1
Id: a50e5204-878e-4b5d-82fb-e6148d976bf7
RecreateDirectories: true
Targets:
    -
        Name: Sophos Logs (XP)
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\Sophos\Sophos *\Logs\
        Recursive: true
        Comment: "Includes Anti-Virus, Client Firewall, Data Control, Device Control, Endpoint Defense, Network Threat Detection, Management Communications System, Patch Control, Tamper Protection"
    -
        Name: Sophos Logs
        Category: Antivirus
        Path: C:\ProgramData\Sophos\*\Logs\
        Recursive: true
        Comment: "Includes Anti-Virus, Client Firewall, Data Control, Device Control, Endpoint Defense, Network Threat Detection, Management Communications System, Patch Control, Tamper Protection"
    -
        Name: Sophos Logs
        Category: Antivirus
        Path: C:\ProgramData\Sophos\Logs\
        Recursive: true
        Comment: "Contains SophosUnifiedSupport.log"
    -
        Name: Sophos Application Events
        Category: Antivirus
        Path: ApplicationEvents.tkape
        Comment: "Event source: Sophos Anti-Virus"

# Documentation
# https://support.sophos.com/support/s/article/KB-000033591?language=en_US
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
