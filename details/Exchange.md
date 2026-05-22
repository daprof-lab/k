# 🎯 **Exchange**
### `File Name: Exchange.tkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Keith Twombley  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Exchange Log Files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Exchange to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Exchange events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Exchange storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Exchange Log Files
Author: Keith Twombley
Version: 1.1
Id: 1b54aafe-5074-4d45-b129-29107ce7f863
RecreateDirectories: true
Targets:
    -
        Name: Exchange client access log files
        Category: Logs
        Path: ExchangeClientAccess.tkape
    -
        Name: Exchange TransportRoles log files
        Category: Logs
        Path: ExchangeTransport.tkape
    -
        Name: Exchange Setup log file
        Category: Logs
        Path: ExchangeSetupLog.tkape

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Targets](../compound_targets.md)
