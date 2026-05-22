# 🎯 **Fsecure**
### `File Name: FSecure.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
F-Secure Antivirus Data

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Fsecure to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Fsecure events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Fsecure storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: F-Secure Antivirus Data
Author: Drew Ervin
Version: 1.0
Id: 8bfd6f82-f867-4ce2-89ac-22802ff9a15f
RecreateDirectories: true
Targets:
    -
        Name: F-Secure Logs
        Category: Antivirus
        Path: C:\ProgramData\F-Secure\Log\
        Recursive: true
    -
        Name: F-Secure User Logs
        Category: Antivirus
        Path: C:\Users\%user%\AppData\Local\F-Secure\Log\
        Recursive: true
    -
        Name: F-Secure Scheduled Scan Reports
        Category: Antivirus
        Path: C:\ProgramData\F-Secure\Antivirus\ScheduledScanReports\
        Recursive: true

# Documentation
# https://community.f-secure.com/en/discussion/122488/removing-f-secure-log-files-from-internet-security
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
