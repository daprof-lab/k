# 🎯 **Mouse Without Borders**
### `File Name: MouseWithoutBorders.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mohamed Sultan  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Mouse Without Borders

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Mouse Without Borders to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Mouse Without Borders events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Mouse Without Borders storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Mouse Without Borders
Author: Mohamed Sultan
Version: 1.0
Id: 89fe72e3-4e58-4125-8e2d-66317f89f8e3
RecreateDirectories: true
Targets:
  - Name: Mouse Without Borders settings - settings.json
    Category: Communications
    Path: C:\Users\%user%\AppData\Local\Microsoft\PowerToys\MouseWithoutBorders
    FileMask: settings.json
    Comment: "Collects the settings file which contains configurations for Mouse Without Borders"

  - Name: Mouse Without Borders Logs folder
    Category: Communications
    Path: C:\Users\%user%\AppData\Local\Microsoft\PowerToys\MouseWithoutBorders\Logs\
    Recursive: true
    FileMask: '*'
    Comment: "Collects the Logs folder for Mouse Without Borders"

  - Name: Mouse Without Borders runtime activity logs
    Category: Communications
    Path: C:\Users\%user%\AppData\Local\Microsoft\PowerToys\MouseWithoutBorders\LogsModuleInterface
    FileMask: '*'
    Comment: "Collects runtime activity logs"

  - Name: Mouse Without Borders msi log - MagicMouse.log
    Category: Communications
    Path: C:\Program Files (x86)\Microsoft Garage\Mouse without Borders
    FileMask: MagicMouse.log
    Comment: "Collects the log file of the Mouse Without Borders MSI version"

# Documentation
# https://0xsultan.github.io/dfir/Exfiltrate-Without-Borders/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
