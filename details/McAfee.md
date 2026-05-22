# 🎯 **Mc Afee**
### `File Name: McAfee.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Sam Smoker  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
McAfee Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mc Afee to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mc Afee events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mc Afee storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: McAfee Log Files
Author: Sam Smoker
Version: 1.1
Id: d2df019b-35d0-4f7b-8132-7500cbd39901
RecreateDirectories: true
Targets:
    -
        Name: McAfee Desktop Protection Logs XP
        Category: Antivirus
        Path: C:\Users\All Users\Application Data\McAfee\DesktopProtection\
        Recursive: true
    -
        Name: McAfee Desktop Protection Logs
        Category: Antivirus
        Path: C:\ProgramData\McAfee\DesktopProtection\
        Recursive: true
    -
        Name: McAfee Endpoint Security Logs
        Category: Antivirus
        Path: C:\ProgramData\McAfee\Endpoint Security\Logs\
        Recursive: true
    -
        Name: McAfee Endpoint Security Logs
        Category: Antivirus
        Path: C:\ProgramData\McAfee\Endpoint Security\Logs_Old\
        Recursive: true
    -
        Name: McAfee VirusScan Logs
        Category: Antivirus
        Path: C:\ProgramData\Mcafee\VirusScan\
        Recursive: true
    -
        Name: McAfee MSC Logs
        Category: Antivirus
        Path: C:\ProgramData\Mcafee\MSC\Logs
        Recursive: true
    -
        Name: McAfee Agent Events
        Category: Antivirus
        Path: C:\ProgramData\Mcafee\Agent\AgentEvents
        Recursive: true
    -
        Name: McAfee Agent Logs
        Category: Antivirus
        Path: C:\ProgramData\Mcafee\Agent\logs
        Recursive: true
    -
        Name: McAfee Data Reputation Logs
        Category: Antivirus
        Path: C:\ProgramData\Mcafee\datareputation\Logs
        Recursive: true
    -
        Name: McAfee Managed VirusScan
        Category: Antivirus
        Path: C:\ProgramData\Mcafee\Managed\VirusScan\Logs
        Recursive: true
    -
        Name: McAfee Agent Events XP
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\McAfee\Common Framework\AgentEvents
        Recursive: true
    -
        Name: McAfee MC Logs XP
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\McAfee\MCLOGS\SAE
        Recursive: true
    -
        Name: McAfee Data Reputation Logs XP
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\McAfee\datreputation\Logs
        Recursive: true
    -
        Name: McAfee Managed VirusScan Logs XP
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\McAfee\Managed\VirusScan\Logs
        Recursive: true
    -
        Name: McAfee WCF Service Logs
        Category: Antivirus
        Path: C:\Program Files (x86)\McAfee\DLP\WCF Service\Log
        Recursive: true

# Documentation
# N/A
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
