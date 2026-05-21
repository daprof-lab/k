# ⚙️ **VLC Recent Files Parser**
### `File Name: VLSeeRecent_VLCRecentFiles.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Charlie Rubisoff  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts the timeline of recently played videos and media paths from VLC history files.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run VLC Recent Files Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw VLC Recent Files Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage VLC Recent Files Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'VLC Recent Files Parser'
Category: FileKnowledge
Author: Charlie Rubisoff
Version: 1.0
Id: 43632314-7e65-4730-91ac-b46e45487468
BinaryUrl: https://github.com/northloopforensics/VL_See_Recent/releases
ExportFormat: txt
Processors:
    -
        Executable: VL_See_Recent.exe
        CommandLine: "%sourceDirectory% %destinationDirectory%"
        ExportFormat: txt

# Documentation
# https://github.com/northloopforensics/VL_See_Recent
# Executable to parse recent file activity from the VLC vlc-qt-interface.ini file.
# This program was written for use on Kroll's KAPE tool. Download the release and then copy the #executable to: kape\Modules\bin
# The tool parses: The file patch for each user's ini file and their recent play history.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
