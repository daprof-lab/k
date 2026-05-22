# ⚙️ **Truffle Hog Secrets**
### `File Name: TruffleHog_Secrets.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Aashiq Ahmed  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Run TruffleHog against collected artifacts to detect potential secrets

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Truffle Hog Secrets to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Truffle Hog Secrets logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Truffle Hog Secrets timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Run TruffleHog against collected artifacts to detect potential secrets
Category: Credentials
Author: Aashiq Ahmed
Version: 1.0
Id: 41f5c5e8-7a5b-4b3e-9c3d-2d8f3a9d4b72
BinaryUrl: https://github.com/trufflesecurity/trufflehog/releases/latest
ExportFormat: json

Processors:
  -
    Executable: TruffleHog\trufflehog.exe
    CommandLine: filesystem "%sourceDirectory%" --json > "%destinationDirectory%\trufflehog_results.json"
    ExportFormat: json

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
