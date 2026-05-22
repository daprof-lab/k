# 🎯 **Avira Avlogs**
### `File Name: AviraAVLogs.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Fabian Murer and Dhiral Panjwani  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Avira Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Avira Avlogs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Avira Avlogs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Avira Avlogs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Avira Logs
Author: Fabian Murer and Dhiral Panjwani
Version: 1.1
Id: f977c6c9-378b-4812-a5ca-1f6c5fe57b18
RecreateDirectories: true
Targets:
    -
        Name: Avira Activity Logs
        Category: Antivirus
        Path: C:\ProgramData\Avira\Antivirus\LOGFILES\
        Recursive: true
        Comment: "Collects the scan logs of Avira Antivirus"
    -
        Name: Avira Security Logs
        Category: Antivirus
        Path: C:\ProgramData\Avira\Security\Logs
        Recursive: true
    -
        Name: Avira VPN Logs
        Category: Antivirus
        Path: C:\ProgramData\Avira\VPN
        Recursive: true
        Comment: "Collects the VPN logs"

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
