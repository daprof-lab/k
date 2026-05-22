# ⚙️ **Tzworks Jmp64 Jumplists**
### `File Name: TZWorks_jmp64_Jumplists.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using jmp64.exe to parse Windows Jumplists from %APPDATA%\Microsoft\Windows\Recent\AutomaticDestinations and %APPDATA%\Microsoft\Windows\Recent\CustomDestinations. Jumplists provides an indication of recent items accessed by each application.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Jmp64 Jumplists to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Jmp64 Jumplists logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Jmp64 Jumplists timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using jmp64.exe to parse Windows Jumplists from %APPDATA%\Microsoft\Windows\Recent\AutomaticDestinations and %APPDATA%\Microsoft\Windows\Recent\CustomDestinations. Jumplists provides an indication of recent items accessed by each application.'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: 43789728-fc3e-4695-980d-29a46e04ff0b
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=20
FileMask: regex:(*.automaticDestinations-ms|*.customDestinations-ms)
ExportFormat: csv
Processors:
    -
        Executable: jmp64.exe
        CommandLine: -cmdfile -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -enumdir %sourceDirectory% -num_subdirs 8 -filter "*.automaticDestinations-ms|*.customDestinations-ms"
        ExportFormat: csv
        ExportFile: Jumplists_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
