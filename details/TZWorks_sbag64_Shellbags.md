# ⚙️ **Tzworks Sbag64 Shellbags**
### `File Name: TZWorks_sbag64_Shellbags.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using sbag64.exe to parse Shellbags from NTUSER.DAT and USRCLASS.DAT. Shellbags can be used to identify files accessed, deleted by the user; storage devices - internal, external or network - where the remote folders were located. The ShellNoRoam\BagXxx key(s) has data for local folders, and the Shell\BagXxx key(s) has data for the remote folders.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Sbag64 Shellbags to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Sbag64 Shellbags logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Sbag64 Shellbags timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using sbag64.exe to parse Shellbags from NTUSER.DAT and USRCLASS.DAT. Shellbags can be used to identify files accessed, deleted by the user; storage devices - internal, external or network - where the remote folders were located. The ShellNoRoam\BagXxx key(s) has data for local folders, and the Shell\BagXxx key(s) has data for the remote folders.'
Category: File_Accessed
Author: Ajith Ravindran
Version: 0.1
Id: 52b151d4-cf93-4616-8e88-b9efe05aee91
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=19
FileMask: (NTUSER.DAT|USRCLASS.DAT)
ExportFormat: csv
Processors:
    -
        Executable: sbag64.exe
        CommandLine: -hive %sourceFile% -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Shellbags_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
