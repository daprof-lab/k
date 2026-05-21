# ⚙️ **Notepad Master Parser**
### `File Name: WindowsNotepadParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** ogmini  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Comprehensive parser targeting Windows 11 Notepad tab states and window geometry histories.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Notepad Master Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Notepad Master Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Notepad Master Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Gathers and parses Windows Notepad Tab State and Window State
Category: LiveResponse
Author: ogmini
Version: 1.0
Id: 1a717e09-5437-4690-9133-922a54f666eb
BinaryUrl: https://github.com/ogmini/Notepad-State-Library/releases
ExportFormat: csv
Processors:
    -
        Executable: WindowsNotepadParser\WindowsNotepadParser-Minimal.exe
        CommandLine: "-o %destinationDirectory%\\Notepad\\"
        ExportFormat: csv

# Documentation
# https://github.com/ogmini/Notepad-State-Library
# Can be useful in a Live Response situation in order to retrieve Unsaved Buffer Chunks
# from Windows Notepad. More details and information can be found in the GitHub Repo.
# Installation:
# Download the latest release for WindowsNotepadParser-Minimal-v#.#.3-standalone
# Create a "WindowsNotepadParser" folder in \Modules\bin
# Place files in \Modules\bin\WindowsNotepadParser folder
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
