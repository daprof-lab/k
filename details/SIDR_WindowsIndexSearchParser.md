# ⚙️ **SIDR Windows Index Search Parser**
### `File Name: SIDR_WindowsIndexSearchParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein (sure[secure])  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
SIDR - Windows index search parser, designed to parse Windows search artifacts from Windows 10 (and prior) and Windows 11 systems

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run SIDR Windows Index Search Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw SIDR Windows Index Search Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage SIDR Windows Index Search Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: SIDR - Windows index search parser, designed to parse Windows search artifacts from Windows 10 (and prior) and Windows 11 systems
Category: LiveResponse
Author: Georg Lauenstein (sure[secure])
Version: 1.0
Id: fcc4bbdd-44ab-4e8f-8a37-d35a9dced850
BinaryUrl: https://github.com/strozfriedberg/sidr
ExportFormat: csv
Processors:
    -
        Executable: sidr.exe
        CommandLine: -f csv %sourceDirectory% -o %destinationDirectory%
        ExportFormat: csv

# Documentation
# https://github.com/strozfriedberg/sidr
# https://www.aon.com/cyber-solutions/aon_cyber_labs/windows-search-index-the-forensic-artifact-youve-been-searching-for/
# https://github.com/AndrewRathbun/DFIRArtifactMuseum/tree/main/Windows%2FWindowsSearchDB
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
