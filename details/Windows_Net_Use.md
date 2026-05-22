# ⚙️ **Windows Net Use**
### `File Name: Windows_Net_Use.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** piesecurity  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Gathers Basic System Information Using the Net Command (Use)

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Net Use to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Net Use logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Net Use timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers Basic System Information Using the Net Command (Use)
Category: LiveResponse
Author: piesecurity
Version: 1.0
Id: 979b4a71-abf8-4f0b-9b94-51e9c1384888
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\net.exe
        CommandLine: Use
        ExportFormat: txt
        ExportFile: NetSystemInfo.txt
        Append: true
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
