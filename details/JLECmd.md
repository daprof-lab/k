# ⚙️ **JLECmd Jump List Parser**
### `File Name: JLECmd.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Runs JLECmd to process taskbar Jump Lists, recovering pinned applications and recent user document browsing habits.

---

## 🔍 **Investigative Use-Cases**
* **Recent Application Profiling**: Timeline application launching patterns from taskbar shortcuts, identifying hidden applications run by users.
* **User Intent Determination**: Establish user intent by tracking frequently opened spreadsheets, documents, or custom admin consoles.
* **Access Time Reconstruction**: Verify precise access timings for files and targets via AutomaticDestinations logs.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'JLECmd: process jumplist files'
Category: FileFolderAccess
Author: Eric Zimmerman
Version: 1.1
Id: 81fe4336-eb10-4733-a770-cb57ec9bd108
BinaryUrl: https://download.ericzimmermanstools.com/JLECmd.zip
ExportFormat: csv
Processors:
    -
        Executable: JLECmd.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory% -q --mp
        ExportFormat: csv
    -
        Executable: JLECmd.exe
        CommandLine: -d %sourceDirectory% --html %destinationDirectory% -q --mp
        ExportFormat: html
    -
        Executable: JLECmd.exe
        CommandLine: -d %sourceDirectory% --json %destinationDirectory% -q --mp
        ExportFormat: json

# Documentation
# https://github.com/EricZimmerman/JLECmd
# https://binaryforay.blogspot.com/2016/03/introducing-jlecmd.html
# https://www.youtube.com/watch?v=wu4-nREmzGM
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://digital-forensics.sans.org/media/EricZimmermanCommandLineToolsCheatSheet-v1.0.pdf
# https://leanpub.com/eztoolsmanuals
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
