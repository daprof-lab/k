# 🎯 **Net Monitorfor Employees Professional**
### `File Name: NetMonitorforEmployeesProfessional.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Tristan PINCEAUX - CERT CWATCH - ALMOND  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Net Monitor for Employees Pro

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Net Monitorfor Employees Professional to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Net Monitorfor Employees Professional events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Net Monitorfor Employees Professional storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Net Monitor for Employees Pro
Author: Tristan PINCEAUX - CERT CWATCH - ALMOND
Version: 1.0
Id: f944d8e5-e7c6-49ac-9c26-b1360fa518cc
RecreateDirectories: true
Targets:
    -
        Name: Net Monitor Server Logs
        Category: ApplicationLogs
        Path: C:\ProgramData\Net Monitor for Employees Pro\log\%user%\
        Recursive: true
        Comment: "Contains Net Monitor server logs"

    -
        Name: Net Monitor Server Data
        Category: Communications
        Path: C:\ProgramData\Net Monitor for Employees Pro\data\
        Recursive: true
        Comment: "Contains Net Monitor server data - Indicates what have been seen as the attacker"

    -
        Name: Net Monitor Server Config
        Category: Apps
        Path: C:\ProgramData\Net Monitor for Employees Pro\config\
        Recursive: true
        Comment: "Contains Net Monitor server config"

    -
        Name: Net Monitor Server Temp Folder
        Category: Apps
        Path: C:\ProgramData\Net Monitor for Employees Pro\tmp\
        Recursive: true

    -
        Name: Net Monitor Client Logs
        Category: ApplicationLogs
        Path: C:\Program Files*\Net Monitor for Employees Pro\log\
        Recursive: true
        Comment: "Contains Net Monitor client logs"

    -
        Name: Net Monitor Client Config
        Category: ApplicationLogs
        Path: C:\Program Files*\Net Monitor for Employees Pro\config\
        Recursive: true
        Comment: "Contains Net Monitor client config"

# Documentation
# https://networklookout.com/
# https://networklookout.com/doc/NetMonitorForEmployees.pdf
# Net Monitor for employees is a monitoring software for office, that allows live screen monitoring and employee activity tracking.
# It can be used as remote access tool, to control applications and processes, to fetch and drop files on target, and to deploy further malicious binaries.
# It can also be used as a keylogger to collect further credentials on compromised targets.
# We have seen this tool used in financial scam and data theft.
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
