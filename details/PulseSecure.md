# 🎯 **Pulse Secure**
### `File Name: PulseSecure.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Paul CABON CERT Cwatch Almond  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Pulse Secure

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Pulse Secure to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Pulse Secure events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Pulse Secure storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Pulse Secure
Author: Paul CABON CERT Cwatch Almond
Version: 1.0
Id: d4ccca86-6e2e-4461-a804-4b0d4f60929b
RecreateDirectories: true
Targets:
    -
        Name: Pulse Secure logs in Programmes Files
        Category: Apps
        Path: C:\Program Files (x86)\Pulse Secure\Logging
        Recursive: true
        FileMask: '*'
        Comment: "Logs for Pule Secure"
    -
        Name: Pulse Secure logs in ProgramData
        Category: Apps
        Path: C:\ProgramData\Pulse Secure\Logging
        Recursive: true
        FileMask: '*'
        Comment: "Logs for Pule Secure"
    -
        Name: Pulse Secure setup logs
        Category: Apps
        Path: C:\Users\*\AppData\Roaming\Pulse Secure\Setup Client
        Recursive: true
        FileMask: '*.log'
        Comment: "Setup logs for Pule Secure"
    -
        Name: Pulse Secure PSAL logs
        Category: Apps
        Path: C:\Users\*\AppData\Local\Pulse Secure\Logging
        FileMask: 'PulseClient.log'
        Comment: "PSAL logs"

# Documentation
# https://help.ivanti.com/ps/help/en_US/ISAC/vNow/cscg/setup_files_for_win_log_file_location.htm
# https://forums.ivanti.com/s/article/How-to-collect-PSAL-Setup-Client-Log-Files-from-Windows-OS?language=en_US
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
