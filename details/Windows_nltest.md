# ⚙️ **Windows Nltest**
### `File Name: Windows_nltest.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Max Zabuty  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects Domain Information

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Nltest to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Nltest logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Nltest timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collects Domain Information
Category: LiveResponse
Author: Max Zabuty
Version: 1.0
Id: 38eedacb-191a-43cf-aaf1-ff183c63c2e9
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\nltest.exe
        CommandLine: /trusted_domains
        ExportFormat: txt
        ExportFile: DomainInformation.txt

# Documentation
# https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731935(v=ws.11)
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
