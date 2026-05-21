# ⚙️ **Master KAPE Automation**
### `File Name: KAPE_Automation.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Brian Maloney  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs a fully integrated suite of analytical parsers to process a complete triage folder.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Master KAPE Automation to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Master KAPE Automation logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Master KAPE Automation timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Module to run for KAPE automation'
Category: --module
Author: Brian Maloney
Version: 1.0
Id: 06cfa868-31f3-43e9-826a-abd199987770
ExportFormat: ""
Processors:
    -
        Executable: C:\Windows\System32\cmd.exe
        CommandLine: /c copy NUL %destinationDirectory%\"%module%" & echo | set /p=%mvar% > %destinationDirectory%\"%module%"
        ExportFormat: ""

# Documentation
# Usage:
# %module% is a comma separated list of modules you want to run on a collection
# %mvar% Provide a list of key:value pairs to be used for variable replacement in modules. Multiple pairs should be separated by ◙
# Example: kape.exe --tsource c --target !SANS_Triage --module KAPE_Automation --mvars module:Mini_Timeline,Mini_Timeline_Slice_by_Daterange^mvar:computerName:laptop◙dateRange:01/01/2020-02/01/2020
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
