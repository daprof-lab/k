# ⚙️ **Windows Klist**
### `File Name: Windows_klist.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gets Kerberos Tickets

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Klist to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Klist logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Klist timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gets Kerberos Tickets
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: e9af32c1-2a2c-4d96-9798-f6829681da83
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\klist.exe
        CommandLine: ""
        ExportFormat: txt
        ExportFile: KerberosTickets.txt

# Documentation
# https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/klist
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
