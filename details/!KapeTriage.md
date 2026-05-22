# 🎯 **Kape Triage**
### `File Name: !KapeTriage.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Phill Moore  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Calls Kape Triage

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Kape Triage to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Kape Triage events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Kape Triage storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Calls Kape Triage
Author: Phill Moore
Version: 1.0
Id: c044913c-d4f8-4d8f-8942-94b6518b60ed
RecreateDirectories: true
Targets:
    -
        Name: KapeTriage
        Category: Triage
        Path: KapeTriage.tkape

# Documentation:
# N/A
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
