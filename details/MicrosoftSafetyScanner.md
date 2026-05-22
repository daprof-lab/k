# 🎯 **Microsoft Safety Scanner**
### `File Name: MicrosoftSafetyScanner.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Geir Olav Skei  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Microsoft Safety Scanner

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Microsoft Safety Scanner to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Microsoft Safety Scanner events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Microsoft Safety Scanner storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Microsoft Safety Scanner
Author: Geir Olav Skei
Version: 1.0
Id: 8e425594-c433-4017-adcd-f5bbcde12492
RecreateDirectories: true
Targets:
    -
        Name: Windows Safety Scanner Logs
        Category: Antivirus
        Path: C:\Windows\Debug\
        FileMask: msert.log

# Documentation
# https://learn.microsoft.com/en-us/defender-endpoint/safety-scanner-download
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
