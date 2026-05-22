# ⚙️ **Sys Internals Ps Logged On**
### `File Name: SysInternals_PsLoggedOn.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
PsLoggedOn is an applet that displays both the locally logged on users and users logged on via resources for either the local computer, or a remote one.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Ps Logged On to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Ps Logged On logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Ps Logged On timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: PsLoggedOn is an applet that displays both the locally logged on users and users logged on via resources for either the local computer, or a remote one.
Category: LiveResponse
Author: Andy Furnas
Version: 1.0
Id: 7b71f318-468e-4616-9ed2-dfd750b6b960
BinaryUrl: https://download.sysinternals.com/files/PSTools.zip
ExportFormat: txt
Processors:
    -
        Executable: PsLoggedon.exe
        CommandLine: -accepteula
        ExportFormat: txt
        ExportFile: PsLoggedOn.txt

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/psloggedon
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
