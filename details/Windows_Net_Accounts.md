# ⚙️ **Windows Net Accounts**
### `File Name: Windows_Net_Accounts.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command (Accounts)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Net Accounts to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Net Accounts logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Net Accounts timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command (Accounts)
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: 6ec49720-1afc-4b89-9454-1398430cb31f
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\net.exe
        CommandLine: Accounts
        ExportFormat: txt
        ExportFile: NetSystemInfo.txt
        Append: true

# Documentation
# https://docs.microsoft.com/en-us/windows/win32/winsock/net-exe-2
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
