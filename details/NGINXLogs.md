# 🎯 **Nginxlogs**
### `File Name: NGINXLogs.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Eric Capuano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NGINX Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Nginxlogs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Nginxlogs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Nginxlogs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: NGINX Log Files
Author: Eric Capuano
Version: 1.0
Id: d5c2cfd9-a8a5-400e-8be5-a8e9b5653a51
RecreateDirectories: true
Targets:
    -
        Name: NGINX Log Files
        Category: Logs
        Path: C:\nginx\logs\
        FileMask: '*.log'

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
