# 🎯 **Mc Afee E PO**
### `File Name: McAfee_ePO.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Doug Metz  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
McAfee ePO Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mc Afee E PO to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mc Afee E PO events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mc Afee E PO storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: McAfee ePO Log Files
Author: Doug Metz
Version: 1.0
Id: 8e893785-6bf2-4990-a783-35b0f5e1b442
RecreateDirectories: true
Targets:
    -
        Name: McAfee ePO Logs
        Category: Antivirus
        Path: C:\ProgramData\McAfee\Endpoint Security\Logs\
        Recursive: true
    -
        Name: McAfee ePO Apache Logs
        Category: Antivirus
        Path: C:\Program Files (x86)\McAfee\ePolicy Orchestrator\Apache2\Logs
        Recursive: true
    -
        Name: McAfee ePO DB Events
        Category: Antivirus
        Path: C:\Program Files (x86)\McAfee\ePolicy Orchestrator\DB\Events
        Recursive: true
    -
        Name: McAfee ePO DB Debug Events
        Category: Antivirus
        Path: C:\Program Files (x86)\McAfee\ePolicy Orchestrator\DB\Events\Debug
        Recursive: true
    -
        Name: McAfee ePO Server Logs
        Category: Antivirus
        Path: C:\Program Files (x86)\McAfee\ePolicy Orchestrator\Server\Logs
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
