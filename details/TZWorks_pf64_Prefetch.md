# ⚙️ **Tzworks Pf64 Prefetch**
### `File Name: TZWorks_pf64_Prefetch.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using pf64.exe to parse Prefetch files from C:\Windows\Prefetch folder. Prefetch files, while tracking GUI AND Command Line based executions; it captures the number times the application was executed, last 8 timestamps of executions and the files and directories accessed by the application for upto 1st 10 seconds

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Pf64 Prefetch to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Pf64 Prefetch logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Pf64 Prefetch timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using pf64.exe to parse Prefetch files from C:\Windows\Prefetch folder. Prefetch files, while tracking GUI AND Command Line based executions; it captures the number times the application was executed, last 8 timestamps of executions and the files and directories accessed by the application for upto 1st 10 seconds'
Category: ProgramExecution
Author: Ajith Ravindran
Version: 0.1
Id: 3e90ee36-7b19-4787-a8af-438d15e6e417
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=1
ExportFormat: csv
Processors:
    -
        Executable: pf64.exe
        CommandLine: -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -pf_path -enumdir %sourceDirectory% -num_subdirs 2 -filter "*.pf"
        ExportFormat: csv
        ExportFile: Prefetch_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
