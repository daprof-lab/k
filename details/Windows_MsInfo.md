# ⚙️ **Windows Ms Info**
### `File Name: Windows_MsInfo.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** NVISO (@NVISOsecurity)  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
msinfo

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Ms Info to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Ms Info logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Ms Info timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: msinfo
Category: LiveResponse
Author: NVISO (@NVISOsecurity)
Version: 0.1
Id: a282bf61-d47b-456c-8b37-a4d455c3e122
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\msinfo32.exe
        CommandLine: /report %destinationDirectory%\msinfo.txt
        ExportFormat: txt

# Documentation
# https://support.microsoft.com/en-us/topic/description-of-microsoft-system-information-msinfo32-exe-tool-10d335d8-5834-90b4-8452-42c58e61f9fc
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
