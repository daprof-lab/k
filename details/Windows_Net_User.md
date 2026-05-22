# ⚙️ **Windows Net User**
### `File Name: Windows_Net_User.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command (User)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Net User to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Net User logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Net User timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command (User)
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: 12589aca-921f-42a0-8806-5174bfa511fd
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\net.exe
        CommandLine: User
        ExportFormat: txt
        ExportFile: NetSystemInfo.txt
        Append: true

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/winsock/net-exe-2
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
