# ⚙️ **Tzworks Lp64 Shortcuts**
### `File Name: TZWorks_lp64_Shortcuts.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using lp64.exe to parse Windows Shortcut files from %APPDATA%\Microsoft\Windows\Recent\ folder. .LNK files can be used to determine the 1st and last time a file or folder was accessed; .LNK files also track the Machine ID and MAC address on the host where the LNK file was created along with the drive type and the drive serial number.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Lp64 Shortcuts to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Lp64 Shortcuts logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Lp64 Shortcuts timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using lp64.exe to parse Windows Shortcut files from %APPDATA%\Microsoft\Windows\Recent\ folder. .LNK files can be used to determine the 1st and last time a file or folder was accessed; .LNK files also track the Machine ID and MAC address on the host where the LNK file was created along with the drive type and the drive serial number.'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: 9382dfec-555e-409a-bc8f-99144bcd5ac6
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=20
ExportFormat: csv
Processors:
    -
        Executable: lp64.exe
        CommandLine: -cmdfile -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -enumdir %sourceDirectory% -num_subdirs 7 -filter "*.lnk"
        ExportFormat: csv
        ExportFile: Shortcuts_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
