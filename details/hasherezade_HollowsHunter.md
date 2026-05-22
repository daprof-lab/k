# ⚙️ **Hasherezade Hollows Hunter**
### `File Name: hasherezade_HollowsHunter.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Jonas A. Wendorf  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
HollowsHunter

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hasherezade Hollows Hunter to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hasherezade Hollows Hunter logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hasherezade Hollows Hunter timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'HollowsHunter'
Category: HollowsHunter
Author: Jonas A. Wendorf
Version: 1.0
Id: a3916582-d43a-4b19-b4f5-c31e65d6daf2
BinaryUrl: https://github.com/hasherezade/hollows_hunter/releases
ExportFormat: json
Processors:
    -
        Executable: hollows_hunter.exe
        CommandLine: /dir "%destinationDirectory%"
        ExportFormat: json

# Documentation
# https://github.com/hasherezade/hollows_hunter
# https://securityliterate.com/extracting-malware-from-memory-with-hollows-hunter/
# HollowsHunter Scans all running processes. Recognizes and dumps a variety of potentially malicious implants (replaced/implanted PEs, shellcodes, hooks, in-memory patches).
# By default only replaced/implanted PEs are detected.
# In order for this module to work, place hollows_hunter.exe and pe-sieve.dll in the Modules/bin folder
# Expected Results:
# If replaced/implanted PEs are detected: The HollowsHunter folder will have the related process information (summary.json and report.json) as well as dump files
# Otherwise: No HollowsHunter folder will be created
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
