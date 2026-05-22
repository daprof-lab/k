# 🎯 **Mesh Agent**
### `File Name: MeshAgent.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Geir Olav Skei, Atea IRT  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
MeshAgent log and configuration files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mesh Agent to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mesh Agent events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mesh Agent storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: MeshAgent log and configuration files
Author: Geir Olav Skei, Atea IRT
Version: 1.0
Id: a96457f4-a65e-42bb-8bc8-6ac3df680689
RecreateDirectories: true
Targets:
    -
        Name: MeshAgent .msh (configuration) file
        Category: Apps
        Path: C:\Program Files\Mesh Agent\
        Recursive: true
        FileMask: "*.msh"
        Comment: "Grabs all .msh (config) files present in this folder"
    -
        Name: MeshAgent log file
        Category: Logs
        Path: C:\Program Files\Mesh Agent\
        Recursive: true
        FileMask: "*.log"
        Comment: "Grabs all .log files present in this folder"

# Documentation
# https://github.com/Ylianst/MeshAgent
# https://ylianst.github.io/MeshCentral/meshcentral/agents/
# https://meshcentral.com/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
