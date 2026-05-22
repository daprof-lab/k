# 🎯 **Trend Micro Security**
### `File Name: TrendMicro.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin, Paul Cabon CERT Almond  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Logs documenting detected security alerts, file blocks, and quarantine activities.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Trend Micro Security to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Trend Micro Security events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Trend Micro Security storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Trend Micro Data
Author: Drew Ervin, Paul Cabon CERT Almond
Version: 2.0
Id: 73f8ccea-61cf-4993-aa26-e5cad4f8cc8f
RecreateDirectories: true
Targets:
    -
        Name: Trend Micro Logs
        Category: Antivirus
        Path: C:\ProgramData\Trend Micro\
        Recursive: true
    -
        Name: Trend Micro Security Agent Report Logs
        Category: Antivirus
        Path: C:\Program Files*\Trend Micro\Security Agent\Report\
        FileMask: '*.log'
    -
        Name: Trend Micro Security Agent Connection Logs
        Category: Antivirus
        Path: C:\Program Files*\Trend Micro\Security Agent\ConnLog\
        FileMask: '*.log'
    -
        Name: Trend Micro Quarantine
        Category: Antivirus
        Path: C:\Program Files*\Trend Micro\*\Quarantine\
        FileMask: '*'

# Documentation
# https://docs.trendmicro.com/en-us/enterprise/trend-micro-apex-one-2019-server-online-help/providing-additional/troubleshooting-reso_001/trend_client_program_021.aspx
# https://docs.trendmicro.com/all/ent/tmcm/v3.5/en-us/tmcm_3.5_olh/Template_Files/decrypt_encrypted_quarantine_files.htm
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
