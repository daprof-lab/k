# ⚙️ **Power Shell Log4j**
### `File Name: PowerShell_log4j.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Jochen Meyer, Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Find every Folder related to log4j core .jar extensions

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Log4j to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Log4j logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Log4j timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Find every Folder related to log4j core .jar extensions
Category: LiveResponse
Author: Jochen Meyer, Georg Lauenstein
Version: 1.0
Id: 94c6d3c1-25bc-4948-b626-f5f455f56b6a
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "Get-ChildItem C:\ -Force -Recurse -ErrorAction SilentlyContinue -Attributes !Directory | Where-Object { $_.Name -like '*log4j*'} | ForEach{ $_.FullName | Out-File -FilePath %destinationDirectory%\$env:COMPUTERNAME.txt -Append}"
        ExportFormat: txt

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
