# 🎯 **Web Servers**
### `File Name: WebServers.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Eric Capuano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Logs from all known web server applications and supporting services

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Web Servers to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Web Servers events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Web Servers storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Logs from all known web server applications and supporting services
Author: Eric Capuano
Version: 1.0
Id: 38de27ae-5047-404b-a7e1-3c99071724d5
RecreateDirectories: true
Targets:
    -
        Name: Apache Access Logs
        Category: Logs
        Path: ApacheAccessLog.tkape
    -
        Name: IIS Logs
        Category: Logs
        Path: IISLogFiles.tkape
    -
        Name: NGINX Logs
        Category: Logs
        Path: NGINXLogs.tkape
    -
        Name: MSSQL Error Logs
        Category: Logs
        Path: MSSQLErrorLog.tkape

# Documentation
# A target to run on systems that may be hosting web servers. Helpful in determining whether web application exploitation is a contributing factor.
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
