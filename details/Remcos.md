# 🎯 **Remcos**
### `File Name: Remcos.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** CERT CWATCH - ALMOND  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Remcos RAT

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Remcos to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Remcos events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Remcos storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Remcos RAT
Author: CERT CWATCH - ALMOND
Version: 1.0
Id: 17433c05-5b84-4bbb-9029-094d3b8adb99
RecreateDirectories: true
Targets:
    -
        Name: Remco RAT Default path
        Category: ApplicationLogs
        Path: C:\Users\*\AppData\Roaming\remcos
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat default file - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path - AppData screenshots folder
        Category: ApplicationLogs
        Path: C:\Users\*\AppData\Roaming\screenshots
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path - AppData notess folder
        Category: ApplicationLogs
        Path: C:\Users\*\AppData\Roaming\notess
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path - AppData micrecords folder
        Category: ApplicationLogs
        Path: C:\Users\*\AppData\Roaming\micrecords
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path - AppData hpsupport
        Category: ApplicationLogs
        Path: C:\Users\*\AppData\Roaming\hpsupport
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path
        Category: ApplicationLogs
        Path: C:\ProgramData\remcos
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path - AppData notess
        Category: ApplicationLogs
        Path: C:\ProgramData\notess
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path - AppData screenshots
        Category: ApplicationLogs
        Path: C:\ProgramData\screenshots
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path  - AppData micrecords
        Category: ApplicationLogs
        Path: C:\ProgramData\micrecords
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

    -
        Name: Remco RAT custom path  - AppData hpsupport
        Category: ApplicationLogs
        Path: C:\ProgramData\hpsupport
        FileMask: 'logs*.dat*'
        Comment: "Remco RAT logs.dat custom path - contains debug data and logs relative to the keylogging module"

# Documentation
# Remcos RAT is a lightweight, fast, and highly customizable Remote Administration Tool with a wide array of functionalities.
# This tool permits keylogging and surveillance (including audio recording and screenshots) and is frequently used by threat actors such as FIN7.
# This target collects all known path where this tool was installed during previous campaigns.
# https://www.splunk.com/en_us/blog/security/splunk-fin7-tool-detections-remcos.html
# https://redcanary.com/threat-detection-report/trends/rmm-tools/
# https://www.cyfirma.com/research/exploiting-document-templates-stego-campaign-deploying-remcos-rat-and-agent-tesla/
# https://wazuh.com/blog/using-wazuh-to-detect-remcos-rat/
# https://www.uptycs.com/blog/threat-research-report-team/remcos-rat-uac-0500-pipe-method
# https://www.elastic.co/security-labs/dissecting-remcos-rat-part-one
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
