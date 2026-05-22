# ⚙️ **Triage Hasher**
### `File Name: TriageHasher.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** FlipForensics  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects hashes based on extension and location filter

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Triage Hasher to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Triage Hasher logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Triage Hasher timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Collects hashes based on extension and location filter
Category: LiveResponse
Author: FlipForensics
Version: 1.0
Id: c69467d4-1673-428b-8382-1ab2e448c484
BinaryUrl: https://github.com/FlipForensics/TriageHasher/releases
ExportFormat: csv
Processors:
    -
        Executable: TriageHasher\TriageHasher.exe
        CommandLine: -o %destinationDirectory%
        ExportFormat: csv

# Documentation
# https://github.com/FlipForensics/TriageHasher
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
