# ⚙️ **Bits Parser**
### `File Name: BitsParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Tool to parse Windows Background Intelligent Transfer Service database files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Bits Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Bits Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Bits Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Tool to parse Windows Background Intelligent Transfer Service database files
Category: GitHub
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: acdc62ed-b1a1-426f-8d5e-e53687284410
BinaryUrl: https://github.com/conexioninversa/BitsParser/blob/master/BitsParser.exe
ExportFormat: json
Processors:
    -
        Executable: BitsParser.exe
        CommandLine: -i %sourceDirectory%\C\ProgramData\Microsoft\Network\Downloader\qmgr.db -o %destinationDirectory%\BitsParser_Results.json
        ExportFormat: json

# Documentation
# https://github.com/fireeye/BitsParser
# By default BitsParser will process files in the %ALLUSERSPROFILE%\Microsoft\Network\Downloader. The script can be used with offline files from alternate operating systems.
# By default BitsParser will only parse and output active jobs and files. To carve deleted entries from the database use --carvedb. To carve entries from all file types, including transaction logs, use --carveall
# https://www.sans.org/reading-room/whitepapers/forensics/bits-forensics-39195
# https://cyberforensicator.com/2019/05/12/using-mitre-attck-for-forensics-bits-jobs-t1197/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
