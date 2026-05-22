# ⚙️ **Windows Hello2hashcat**
### `File Name: Windows_Hello2Hashcat.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Kevin Pagano  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Windows Hello 2 Hashcat

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Hello2hashcat to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Hello2hashcat logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Hello2hashcat timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Windows Hello 2 Hashcat'
Category: Windows
Author: Kevin Pagano
Version: 1.0
Id: 07a020cc-ef74-4746-bcf9-04c6575ec4a4
BinaryUrl: https://github.com/Banaanhangwagen/WINHELLO2hashcat
ExportFormat: txt
Processors:
    -
        Executable: WINHELLO2hashcat.exe
        CommandLine: --windows %sourceDirectory%
        ExportFormat: txt
        ExportFile: winhello_hash.txt

# Documentation
# WINHELLO2hashcat - Extracts "hash" from Windows Hello PIN for cracking in Hashcat
# https://github.com/Banaanhangwagen/WINHELLO2hashcat
# Make sure to have the python package "dpapick3" per the requirements for the .py
# You will need to package the .py to .exe for running in KAPE via https://pypi.org/project/auto-py-to-exe/
# It is recommended to collect with KAPE Target first and then parse the Windows directory as input
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
