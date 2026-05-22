# ⚙️ **Tzworks Ntfswalk64 MFT**
### `File Name: TZWorks_ntfswalk64_MFT.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using ntfswalk64.exe to parse the Master File Table $MFT from the host.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Ntfswalk64 MFT to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Ntfswalk64 MFT logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Ntfswalk64 MFT timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using ntfswalk64.exe to parse the Master File Table $MFT from the host.'
Category: File_Accessed
Author: Ajith Ravindran
Version: 0.1
Id: 2ead153f-47a3-4c44-9081-2635e8d7e5ce
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=12
ExportFormat: csv
FileMask: $MFT
Processors:
    -
        Executable: ntfswalk64.exe
        CommandLine: -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -mftfile %sourceFile%
        ExportFormat: csv
        ExportFile: MFT_Parsed.csv

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
