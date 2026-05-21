# 🎯 **OpenVPN Client Logs**
### `File Name: OpenVPNClient.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mathias Frank  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Remote tunnel configurations, connection handshakes, and OpenVPN client diagnostic logs.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from OpenVPN Client Logs to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate OpenVPN Client Logs events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit OpenVPN Client Logs storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: OpenVPN Client Config and Log
Author: Mathias Frank
Version: 1.0
Id: 03920e05-c794-46d1-b2cd-5e1febd0fdaf
RecreateDirectories: true
Targets:
    -
        Name: OpenVPN Client Config
        Category: ApplicationLogs
        Path: C:\Users\%user%\OpenVPN\config\
        Recursive: true
        Comment: "Contains OpenVPN Configs (Profiles)"
    -
        Name: OpenVPN Client Config
        Category: ApplicationLogs
        Path: C:\Program Files*\OpenVPN\config
        Recursive: true
        Comment: "Contains OpenVPN Configs(Profiles)"
    -
        Name: OpenVPN Client Config
        Category: ApplicationLogs
        Path: C:\Users\%user%\OpenVPN\log\
        FileMask: '*.log'
        Comment: "Contains OpenVPN Logs for each Config(Profile)"

# Documentation
# https://www.researchgate.net/publication/333198144_Analysis_of_Security_Virtual_Private_Network_VPN_Using_OpenVPN
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
