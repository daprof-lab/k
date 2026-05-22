# ⚙️ **Sync KAPE**
### `File Name: Sync_KAPE.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun, Sean Straw, and Isaiah Jensen  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
KAPE: Sync for new Targets/Modules

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Sync KAPE to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Sync KAPE logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Sync KAPE timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'KAPE: Sync for new Targets/Modules'
Category: KAPESync
Author: Andrew Rathbun, Sean Straw, and Isaiah Jensen
Version: 1.3
Id: 371e0944-8025-4690-9c79-15faafa561a9
BinaryUrl: https://s3.amazonaws.com/cyb-us-prd-kape/kape.zip
ExportFormat: ""
Processors:
    -
        Executable: C:\Windows\System32\cmd.exe
        CommandLine: /c "%kapeDirectory%\kape.exe" --sync
        ExportFormat: ""
        ExportFile: Sync_KAPE.txt

# Documentation
# https://github.com/EricZimmerman/KapeFiles
# This Module ensures you have the latest KAPE Targets and Modules prior to running any Modules
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
