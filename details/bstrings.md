# ⚙️ **bstrings Master Scanner**
### `File Name: bstrings.mkape`

{% hint style="info" %}
**Category:** Compound & Automation Packages  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs multiple bstrings modules to extract URLs, emails, and IPs from large data volumes.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run bstrings Master Scanner to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw bstrings Master Scanner logs to index file anomalies.
* **Incident Impact Assessment**: Leverage bstrings Master Scanner timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Run all bstrings Modules
Category: Modules
Author: Andrew Rathbun
Version: 1.0
Id: 5a564195-2de6-422b-904e-312cf2303d2f
BinaryUrl: https://ericzimmerman.github.io/
ExportFormat: txt
Processors:
    -
        Executable: bstrings_Bitlocker.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_CreditCards.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_Email.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_IPv4.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_MACAddresses.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_SSN.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_UNC.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_URLs.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_USPhone.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_WinPath.mkape
        CommandLine: ""
        ExportFormat: ""
    -
        Executable: bstrings_ZipCodes.mkape
        CommandLine: ""
        ExportFormat: ""

# Documentation
# N/A
```
---

[⬅️ Back to Compound & Automation Packages Modules](../compound_modules.md)
