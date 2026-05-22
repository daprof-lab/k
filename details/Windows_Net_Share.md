# ⚙️ **Windows Net Share**
### `File Name: Windows_Net_Share.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command (Share)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Net Share to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Net Share logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Net Share timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command (Share)
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: aba1ed38-d670-4db1-be70-bebb0a6a4ef3
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\net.exe
        CommandLine: Share
        ExportFormat: txt
        ExportFile: NetSystemInfo.txt
        Append: true

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/winsock/net-exe-2
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
