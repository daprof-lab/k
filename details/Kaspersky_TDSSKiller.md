# ⚙️ **Kaspersky Tdsskiller**
### `File Name: Kaspersky_TDSSKiller.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mohamed El-Hadidi  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Shows if the system have either rootkits or bootkits, TDSSKiller tool for detecting and removing rootkits and bootkits

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Kaspersky Tdsskiller to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Kaspersky Tdsskiller logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Kaspersky Tdsskiller timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Shows if the system have either rootkits or bootkits, TDSSKiller tool for detecting and removing rootkits and bootkits
Category: LiveResponse
Author: Mohamed El-Hadidi
Version: 1.0
Id: 38be1e67-e028-4bc0-ac50-376b7875be08
BinaryUrl: http://media.kaspersky.com/utilities/VirusUtilities/EN/tdsskiller.exe
ExportFormat: txt
Processors:
    -
        Executable: TDSSKiller\tdsskiller.exe
        CommandLine: -accepteula -accepteulaksn -sigcheck -tdlfs -silent -l %destinationDirectory%\tdsskiller.txt
        ExportFormat: txt

# Documentation
# Create a folder "TDSSKiller" within the "Modules\bin" KAPE folder
# Place "tdsskiller.exe" file into "Modules\bin\TDSSKiller"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
