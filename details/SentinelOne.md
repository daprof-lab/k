# 🎯 **SentinelOne Logs**
### `File Name: SentinelOne.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Kirtan Shah  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Operational log databases, network diagnostics, and agent states for SentinelOne EDR.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from SentinelOne Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate SentinelOne Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit SentinelOne Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Sentinel One Logs
Author: Kirtan Shah
Version: 1.0
Id: b658aca2-8a69-440d-83ac-b81666a6484d
RecreateDirectories: true
Targets:
    -
        Name: SentinelOne EDR Log
        Category: Antivirus
        Path: C:\programdata\sentinel\logs\
        Recursive: true
        Comment: "Logs are in Binary Format (.binlog)"

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
