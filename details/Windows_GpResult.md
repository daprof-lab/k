# ⚙️ **Windows Gp Result**
### `File Name: Windows_GpResult.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** NVISO (@NVISOsecurity)  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
gpresult

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Gp Result to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Gp Result logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Gp Result timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: gpresult
Category: LiveResponse
Author: NVISO (@NVISOsecurity)
Version: 0.1
Id: 4dc75767-5c10-4ec5-b5d6-ba332f92070f
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\gpresult.exe
        CommandLine: /z
        ExportFormat: txt
        ExportFile: gpresult.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/gpresult
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
