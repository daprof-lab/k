# 🎯 **Manage Engine Logs**
### `File Name: ManageEngineLogs.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Whitney Champion, Phill Moore  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
ManageEngine Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Manage Engine Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Manage Engine Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Manage Engine Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ManageEngine Log Files
Author: Whitney Champion, Phill Moore
Version: 1.1
Id: c034ee17-a97f-48a1-b720-c73867ed66e6
RecreateDirectories: true
Targets:
    -
        Name: ManageEngine Desktop Central Log Files
        Category: Logs
        Path: C:\ManageEngine\DesktopCentral_Server\logs\
        Recursive: true
    -
        Name: ManageEngine ADSelfService Plus Log Files
        Category: Logs
        Path: C:\ManageEngine\ADSelfService Plus\logs\
        Recursive: true

# Documentation
# https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-259a
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
