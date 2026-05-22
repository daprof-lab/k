# ⚙️ **Power Shell Get Do Svc4n6**
### `File Name: PowerShell_Get-DoSvc4n6.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Gabriele Zambelli  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
Get-DoSvc4n6: extracts (amongst others) public IP addresses from DoSvc EventTraceLogs

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Get Do Svc4n6 to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Get Do Svc4n6 logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Get Do Svc4n6 timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Get-DoSvc4n6: extracts (amongst others) public IP addresses from DoSvc EventTraceLogs'
Category: SystemActivity
Author: Gabriele Zambelli
Version: 1.3
Id: fc01eeb0-2e2d-4fbe-96b8-02a64933d466
BinaryUrl: https://raw.githubusercontent.com/forensenellanebbia/powershell-scripts/master/Get-DoSvc4n6.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -Command "& '%kapedirectory%\Modules\bin\Get-DoSvc4n6.ps1' %sourceDirectory% -ExtractAll -SkipIP2Location -OutputPath %destinationDirectory%"
        ExportFormat: csv

# Documentation
# Get-DoSvcExternalIP extracts public IP addresses of a Windows 10 device from DoSvc EventTraceLogs
# https://raw.githubusercontent.com/forensenellanebbia/powershell-scripts/master/Get-DoSvc4n6.ps1
# Get-DoSvc4n6.ps1 must be in Modules\bin folder
# Example: .\kape.exe --msource D:\kape\C --mdest D:\kape\out --module Get-DoSvc4n6
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
