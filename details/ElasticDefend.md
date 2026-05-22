# 🎯 **Elastic Defend**
### `File Name: ElasticDefend.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** AlliedPterodactyl  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Elastic Defend Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Elastic Defend to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Elastic Defend events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Elastic Defend storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Elastic Defend Data
Author: AlliedPterodactyl
Version: 1.0
Id: cfa61264-c9f8-4807-b29c-0ef6236dff6f
RecreateDirectories: true
Targets:
    -
        Name: Elastic Defend Logs
        Category: Antivirus
        Path: C:\Program Files\Elastic\Endpoint\state\log\
        FileMask: '*.log'
    -
        Name: Elastic Defend Quarantine
        Category: Antivirus
        Path: C:\.equarantine\
        FileMask: '*'
    -
        Name: Elastic Defend Quarantine
        Category: Antivirus
        Path: C:\Program Files\Elastic\Endpoint\state\.equarantine\
        FileMask: '*'

# Documentation
# https://www.elastic.co/docs/solutions/security/configure-elastic-defend/configure-an-integration-policy-for-elastic-defend
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
