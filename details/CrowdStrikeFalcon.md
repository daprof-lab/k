# 🎯 **CrowdStrike Falcon**
### `File Name: CrowdStrikeFalcon.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Cardinsou  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Telemetry diagnostic configurations, local cache updates, and installation status from the Falcon agent.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from CrowdStrike Falcon to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate CrowdStrike Falcon events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit CrowdStrike Falcon storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: CrowdStrike Falcon
Author: Cardinsou
Version: 1.0
Id: 1bc262c6-4345-4b2e-8741-ca5f7dbe4871
RecreateDirectories: true
Targets:
    -
        Name: CrowdStrike Falcon Quarantined File
        Category: Antivirus
        Path: C:\Windows\System32\Drivers\CrowdStrike\Quarantine\
        Recursive: true

# Documentation
# https://github.com/cardinsou/Crowdstrike-quarantined-file-decipher
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
