# ⚙️ **Tzworks Jp64 Usnjrnl**
### `File Name: TZWorks_jp64_USNJrnl.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using jp64.exe to parse the Windows Journal File $USNJRNL:$J from the host.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Jp64 Usnjrnl to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Jp64 Usnjrnl logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Jp64 Usnjrnl timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using jp64.exe to parse the Windows Journal File $USNJRNL:$J from the host.'
Category: File_Accessed
Author: Ajith Ravindran
Version: 0.1
Id: 46b6d413-86f1-4336-b28d-49e16e41032d
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=12
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: jp64.exe
        CommandLine: -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -a -file %sourceDirectory%\\$Extend\$J -mftfile %sourceFile%
        ExportFormat: csv
        ExportFile: USNJrnl_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
