# 🎯 **UEMS**
### `File Name: UEMS.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Abdelkarim CHORFI - CERT CWATCH - ALMOND  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
UEMS Manage Engine Agent

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from UEMS to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate UEMS events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit UEMS storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: UEMS Manage Engine Agent
Author: Abdelkarim CHORFI - CERT CWATCH - ALMOND
Version: 1.0
Id: 3ff43bb0-ac44-4374-ac4e-dbe104d81b60
RecreateDirectories: true
Targets:
    -
        Name: Unified endpoint management and security solutions from ManageEngine
        Category: RMM Tool
        Path: C:\Program Files (x86)\ManageEngine\UEMS_Agent\logs
        Recursive: true
        FileMask: '*.log'
        Comment: "Collects all logs for UEMS"

    -
        Name: Unified endpoint management and security solutions from ManageEngine
        Category: RMM Tool
        Path: C:\Users\%user%\AppData\Local\VirtualStore\Program Files (x86)\ManageEngine\UEMS_Agent\logs
        Recursive: true
        FileMask: '*.log'
        Comment: "Collects User logs for UEMS"

# Documentation
# https://www.manageengine.com/unified-endpoint-management-security.html
# UEMS Manage Engine Agent is a remote access tool in the ManageEngine suite.
# We have observed this tool being deployed in a recent Cactus ransomware Campaign:
# https://arcticwolf.com/resources/blog/qlik-sense-exploited-in-cactus-ransomware-campaign/
# https://www.bleepingcomputer.com/news/security/cactus-ransomware-exploiting-qlik-sense-flaws-to-breach-networks/
# https://www.cybersecuritydive.com/news/cactus-ransomware-qlik-sense-cves/714578/
# https://www.linkedin.com/pulse/wheres-my-logs-uems-zoho-meeting-edition-geir-olav-skei-ua2rfv
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
