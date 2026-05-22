# ⚙️ **Windows Schtasks**
### `File Name: Windows_schtasks.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Brian Maloney  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Displays all scheduled tasks

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Schtasks to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Schtasks logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Schtasks timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Displays all scheduled tasks
Category: Persistence
Author: Brian Maloney
Version: 1.2
Id: 66d26feb-6dd7-4b12-b88b-b43ee17cd2c7
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\schtasks.exe
        CommandLine: /Query /V /FO CSV
        ExportFormat: csv
        ExportFile: Scheduled Tasks.csv
    -
        Executable: C:\Windows\System32\schtasks.exe
        CommandLine: /Query /XML
        ExportFormat: xml
        ExportFile: Scheduled Tasks.xml

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/taskschd/schtasks
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/schtasks
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
