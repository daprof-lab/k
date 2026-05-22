# 🎯 **ESET Antivirus**
### `File Name: ESET.tkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Drew Ervin, Phill Moore  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
Event logs, scanned threat metadata, and protection modules status for ESET.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from ESET Antivirus to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate ESET Antivirus events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit ESET Antivirus storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: ESET Antivirus Data
Author: Drew Ervin, Phill Moore
Version: 1.3
Id: 14ac7bff-2d77-4582-8558-73cf75805aaa
RecreateDirectories: true
Targets:
    -
        Name: ESET NOD32 AV Logs (XP)
        Category: Antivirus
        Path: C:\Documents and Settings\All Users\Application Data\ESET\ESET NOD32 Antivirus\Logs\
        Recursive: true
    -
        Name: ESET NOD32 AV Logs
        Category: Antivirus
        Path: C:\ProgramData\ESET\ESET NOD32 Antivirus\Logs\
        Recursive: true
        Comment: "Parser available at https://github.com/laciKE/EsetLogParser"
    -
        Name: ESET NOD32 AV Logs
        Category: Antivirus
        Path: C:\ProgramData\ESET\ESET Security\Logs
        Recursive: true
    -
        Name: ESET Remote Administrator Logs
        Category: Antivirus
        Path: C:\ProgramData\ESET\RemoteAdministrator\Agent\EraAgentApplicationData\Logs
        Comment: "Remote Administrator logs include information on tasks executed on the target."
    -
        Name: Local User Quarantine
        Category: Antivirus
        Path: C:\Users\%user%\AppData\Local\ESET\ESET Security\Quarantine\
        Recursive: true
    -
        Name: SYSTEM user quarantine
        Category: Antivirus
        Path: C:\Windows\System32\config\systemprofile\AppData\Local\ESET\ESET Security\Quarantine\
        Recursive: true

# Documentation
# Remote Administrator log information: https://help.eset.com/protect_admin/80/en-US/fs_agent_connection_troubleshooting.html
```
---

[⬅️ Back to Threat Hunting, AV & Logs Targets](../threat_hunting_targets.md)
