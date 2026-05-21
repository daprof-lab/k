# ⚙️ **PECmd Prefetch Parser**
### `File Name: PECmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman / Andrew Rathbun  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs PECmd to process Windows Prefetch files (.pf), mapping process execution times, loaded DLL lists, and launching directories.

---

## 🔍 **Investigative Use-Cases**
* **Execution Timeline Building**: Generate chronologically sorted timelines of program launches, showing last execution times and run counts.
* **DLL Side-loading Anomaly Check**: Audit DLL loading lists inside Prefetch records to detect malicious DLLs loaded from temp folders.
* **Malware Staged Path Verification**: Retrieve directory pathways where malicious binaries were executed, matching user temp directories.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'PECmd: process prefetch files'
Category: ProgramExecution
Author: Eric Zimmerman and Andrew Rathbun
Version: 1.1
Id: 7ef84a6b-5115-45bb-af2a-3249a3237e75
BinaryUrl: https://download.ericzimmermanstools.com/PECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: PECmd.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory% --mp -q
        ExportFormat: csv
    -
        Executable: PECmd.exe
        CommandLine: -d %sourceDirectory% --html %destinationDirectory% --mp -q
        ExportFormat: html
    -
        Executable: PECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory% --mp -q
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/PECmd
# https://binaryforay.blogspot.com/2016/01/introducing-pecmd.html
# https://www.youtube.com/watch?v=f4RAtR_3zcs
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://leanpub.com/eztoolsmanuals
# --mp added for higher precision timestamps
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
