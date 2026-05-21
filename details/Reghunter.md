# ⚙️ **Reghunter Suite**
### `File Name: Reghunter.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Executes the complete collection of Reghunter parsers against all acquired registry hives.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Reghunter Suite to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Reghunter Suite logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Reghunter Suite timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute all Reghunter modules
Category: Registry
Author: Georg Lauenstein
Version: 1.0
Id: 2701714e-4de8-435b-9d7c-dfe81c3ea22e
ExportFormat: json
Processors:
    -
        Executable: reg_hunter_binary.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_shell.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_encoding.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_link.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_ip.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_email.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_obfuscation.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_script.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_shellcode.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_unc.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_url.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: reg_hunter_suspicious.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
