# 🎯 **Agent Ransack**
### `File Name: AgentRansack.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Agent Ransack - Free File Searching Utility

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Agent Ransack to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Agent Ransack events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Agent Ransack storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Agent Ransack - Free File Searching Utility
Author: Andrew Rathbun
Version: 1.0
Id: b4b0b113-b3d9-4c23-a155-2f879afd03e8
RecreateDirectories: true
Targets:
    -
        Name: Agent Ransack Config Logs
        Category: Software
        Path: C:\Users\%user%\AppData\Roaming\Mythicsoft\AgentRansack\config
        Recursive: true
    -
        Name: Agent Ransack CrashReports Logs
        Category: Software
        Path: C:\Users\%user%\AppData\Roaming\Mythicsoft\AgentRansack\CrashReports
        Recursive: true
    -
        Name: Agent Ransack IndexLog Logs
        Category: Software
        Path: C:\Users\%user%\AppData\Roaming\Mythicsoft\AgentRansack\IndexLog
        Recursive: true
    -
        Name: Agent Ransack Logs
        Category: Software
        Path: C:\Users\%user%\AppData\Roaming\Mythicsoft\AgentRansack\logs
        Recursive: true

# Documentation
# https://www.mythicsoft.com/agentransack/
# https://help.mythicsoft.com/agentransack/v9/en/index.html -> https://help.mythicsoft.com/agentransack/v9/en/folder_settings.htm
# .\AppData\Roaming\Mythicsoft\AgentRansack\config\history.xml - appears to track user's search terms
# .\AppData\Roaming\Mythicsoft\AgentRansack\logs\AgentRansack-app.log - appears to log when searches are conducted, similar to the below:
# 2023.07.13 15:51:16:291 (56020.117972) Starting search
# 2023.07.13 15:51:16:309 (56020.117972) Search started
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
