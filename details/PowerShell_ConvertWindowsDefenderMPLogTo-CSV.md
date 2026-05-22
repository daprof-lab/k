# ⚙️ **Power Shell Convert Windows Defender Mplog To CSV**
### `File Name: PowerShell_ConvertWindowsDefenderMPLogTo-CSV.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ConvertWindowsDefenderMPLogTo-CSV.ps1 - Export Windows Defender MPLog file(s) into CSV file(s).

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Convert Windows Defender Mplog To CSV to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Convert Windows Defender Mplog To CSV logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Convert Windows Defender Mplog To CSV timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: ConvertWindowsDefenderMPLogTo-CSV.ps1 - Export Windows Defender MPLog file(s) into CSV file(s).
Category: Antivirus
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: 3d05c9b5-9c6f-46c3-9203-577f525aad64
BinaryUrl: https://gist.github.com/Qazeer/5ad40f6e98362520290d13f3015f79ec
FileMask: "MPLog-*.log"
ExportFormat: CSV
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\ConvertWindowsDefenderMPLogTo-CSV.ps1' -InputFile '%sourceFile%' -OutputFolder %destinationDirectory%"
        ExportFormat: CSV

# Documentation
# Convert the Windows Defender MPLog file(s) found into CSV file(s).
# The MPLog are roughly parsed, as the log format is very disparate and does not follow a given schema.
# https://gist.github.com/Qazeer/5ad40f6e98362520290d13f3015f79ec
# Information on Windows Defender MPLog for DFIR: https://www.crowdstrike.com/blog/how-to-use-microsoft-protection-logging-for-forensic-investigations/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
