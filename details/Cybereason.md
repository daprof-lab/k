# 🎯 **Cybereason**
### `File Name: Cybereason.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Cybereason Sensor/Detection Logs

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Cybereason to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Cybereason events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Cybereason storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Cybereason Sensor/Detection Logs
Author: piesecurity
Version: 1.0
Id: 73ddfac4-a50a-4fcf-9fa2-7eb360cfd896
RecreateDirectories: true
Targets:
    -
        Name: Cybereason Anti-Ransomware Logs
        Category: Antivirus
        Path: C:\ProgramData\crs1\Logs
        Recursive: true
    -
        Name: Cybereason Sensor Communications and Anti-Malware Logs
        Category: Antivirus
        Path: C:\ProgramData\apv2\Logs
        Recursive: true
    -
        Name: Cybereason Application Control and NGAV Logs
        Category: Antivirus
        Path: C:\ProgramData\crb1\Logs
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
