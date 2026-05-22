# ⚙️ **Windows Net Local Group**
### `File Name: Windows_Net_LocalGroup.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command (LocalGroup)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Net Local Group to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Net Local Group logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Net Local Group timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command (LocalGroup)
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: a9789a17-1061-4a66-b5da-419223bb6c09
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\net.exe
        CommandLine: LocalGroup
        ExportFormat: txt
        ExportFile: NetSystemInfo.txt
        Append: true

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/winsock/net-exe-2
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
