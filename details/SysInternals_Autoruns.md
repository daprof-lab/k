# ⚙️ **Sys Internals Autoruns**
### `File Name: SysInternals_Autoruns.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andy Furnas, Encoding updates by piesecurity, Andreas Hunkeler (@Karneades)  
**Version:** 1.5
{% endhint %}

---

## 📖 **Forensic Description & Value**
Autoruns reports Explorer shell extensions, toolbars, browser helper objects, Winlogon notifications, auto-start services, and much more.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sys Internals Autoruns to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sys Internals Autoruns logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sys Internals Autoruns timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Autoruns reports Explorer shell extensions, toolbars, browser helper objects, Winlogon notifications, auto-start services, and much more.
Category: Persistence
Author: Andy Furnas, Encoding updates by piesecurity, Andreas Hunkeler (@Karneades)
Version: 1.5
Id: c95e71bd-7abb-48c3-abae-f48b9ff19dec
BinaryUrl: https://download.sysinternals.com/files/Autoruns.zip
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "& '%kapedirectory%\Modules\bin\autorunsc.exe' -a * -s -c -accepteula -nobanner -h * | Set-Content -Encoding UTF8 -Path '%destinationDirectory%\Autoruns.csv'"
        ExportFormat: csv

# Documentation
# https://docs.microsoft.com/en-us/sysinternals/downloads/autoruns
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
