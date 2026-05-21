# 🎯 **Windows IPConfig Details**
### `File Name: Windows_IPConfig.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts current network adapter configurations, hardware MACs, and assigned IP ranges.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows IPConfig Details to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows IPConfig Details events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows IPConfig Details storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: IPConfig
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: 5afdfd6b-5ebb-4545-9980-88e6f421e508
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\ipconfig.exe
        CommandLine: /all
        ExportFormat: txt
        ExportFile: ipconfig.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
