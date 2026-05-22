# ⚙️ **WMI Parser**
### `File Name: WMI-Parser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WMI-Parser - parses the WMI object database looking for persistence

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run WMI Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw WMI Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage WMI Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: WMI-Parser - parses the WMI object database looking for persistence
Category: WMI
Author: Andrew Rathbun
Version: 1.0
Id: ab1d6a09-450a-464a-aebc-7f415035404d
BinaryUrl: https://github.com/AndrewRathbun/WMI-Parser/releases/download/v0.0.3/WMI-Parser.zip
ExportFormat: ""
FileMask: OBJECTS.DATA
Processors:
    -
        Executable: wmi-parser\wmi-parser.exe
        CommandLine: -i %sourceFile% -o %destinationDirectory%
        ExportFormat: ""

# Documentation
# Original repo: https://github.com/woanware/wmi-parser
# Updated fork: https://github.com/AndrewRathbun/WMI-Parser
# Make sure you have .NET 6 installed on your machine: https://dotnet.microsoft.com/en-us/download/dotnet/6.0 - download .NET Runtime 6.X.X for console applications only, .NET Desktop Runtime 6.X.X if you have GUI tools that require .NET 6
# Make sure the following files are in your .\KAPE\Modules\bin\wmi-parser folder:
# Wmi-Parser.dll
# Wmi-Parser.exe
# Wmi-Parser.runtimeconfig.json
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
