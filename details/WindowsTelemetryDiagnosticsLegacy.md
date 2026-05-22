# 🎯 **Windows Telemetry Diagnostics Legacy**
### `File Name: WindowsTelemetryDiagnosticsLegacy.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Andrew Rathbun and Josh Mitchell  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Legacy Windows Telemetry and Diagnostics files (*.rbs)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Windows Telemetry Diagnostics Legacy to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Windows Telemetry Diagnostics Legacy events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Windows Telemetry Diagnostics Legacy storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Legacy Windows Telemetry and Diagnostics files (*.rbs)
Author: Andrew Rathbun and Josh Mitchell
Version: 1.0
Id: 4bc4b0bc-9334-4ad8-a331-78c4751ea07d
RecreateDirectories: true
Targets:
    -
        Name: Legacy .rbs files relating to Windows Telemetry and Diagnostics
        Category: SystemEvents
        Path: C:\ProgramData\Microsoft\Diagnosis\
        FileMask: 'events*.rbs'
    -
        Name: Legacy .rbs files relating to Windows Telemetry and Diagnostics
        Category: SystemEvents
        Path: C:\Windows.old\ProgramData\Microsoft\Diagnosis\
        FileMask: 'events*.rbs'

# Documentation
# https://arxiv.org/pdf/2002.12506
# https://www.kroll.com/en/insights/publications/cyber/forensically-unpacking-eventtranscript/eventtranscript-files-and-their-relation-diagtrack
# These .rbs files should simply be opened in a text editor as they are effectively JSON files. These are very similar, if not, identical, to the JSON payloads included in EventTranscript.db
# These files were present in Windows 10 between versions 1507 and 1809. 1709 is when EventTranscript.db came into play.
# This Target should grab the following files:
#
# events00.rbs
# events01.rbs
# events10.rbs
# events11.rbs
# Events_Normal.rbs
# Events_NormalCritical.rbs
# Events_CostDeferred.rbs
# Events_Realtime.rbs
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
