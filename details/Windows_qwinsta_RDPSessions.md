# ⚙️ **Windows Qwinsta Rdpsessions**
### `File Name: Windows_qwinsta_RDPSessions.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Display information about Active Remote Desktop Services sessions. - Query Windows Station

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Qwinsta Rdpsessions to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Qwinsta Rdpsessions logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Qwinsta Rdpsessions timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Display information about Active Remote Desktop Services sessions. - Query Windows Station
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: 7407dd38-cd98-4981-b9ee-d6ae1e306db0
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\qwinsta.exe
        CommandLine: /counter
        ExportFormat: txt
        ExportFile: qwinsta.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/qwinst
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
