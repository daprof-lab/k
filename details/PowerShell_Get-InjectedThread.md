# ⚙️ **Power Shell Get Injected Thread**
### `File Name: PowerShell_Get-InjectedThread.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** piesecurity  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Get-InjectedThread

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Get Injected Thread to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Get Injected Thread logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Get Injected Thread timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Get-InjectedThread'
Category: LiveResponse
Author: piesecurity
Version: 1.1
Id: c3998d96-fa6f-44db-9bb3-4cc66259a09c
BinaryUrl: https://gist.githubusercontent.com/jaredcatkinson/23905d34537ce4b5b1818c3e6405c1d2/raw/104f630cc1dda91d4cb81cf32ef0d67ccd3e0735/Get-InjectedThread.ps1
ExportFormat: json
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -ep bypass -Command "Import-Module '%kapedirectory%\Modules\bin\Get-InjectedThread.ps1' -Force; Get-InjectedThread | ConvertTo-Json  | Out-File -FilePath '%destinationDirectory%\Get-InjectedThread.json'"
        ExportFormat: json

# Documentation
# Get-InjectedThread Memory resident malware (fileless malware) often uses a form of memory injection to get code execution. Get-InjectedThread looks at each running thread to determine if it is the result of memory injection.
# https://gist.githubusercontent.com/jaredcatkinson/23905d34537ce4b5b1818c3e6405c1d2/raw/104f630cc1dda91d4cb81cf32ef0d67ccd3e0735/Get-InjectedThread.ps1
# In order for this module to work, place the powershell script on the modules bin folder
# Expected Results:
# If injected threads are detected: Get-InjectedThread.json in the LiveResponse Folder will have the related process information
# If no injected threads are detected and the script ran successfully: An empty Get-InjectedThread.json will be found in the LiveResponse folder
# If the script failed: No output file will be produced. Most likely due to Get-InjectedThread.json not being found in the modules bin folder
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
