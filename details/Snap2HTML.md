# ⚙️ **Snap2html**
### `File Name: Snap2HTML.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Dennis Reneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Directory Lister - HTML Browser

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Snap2html to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Snap2html logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Snap2html timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Directory Lister - HTML Browser'
Category: DirectoryLister
Author: Dennis Reneau
Version: 1.0
Id: 0ca2b18d-b886-497c-a57a-ea4442c878e2
BinaryUrl: https://www.rlvision.com/script/download.php?ref=rlv.com&file=Snap2HTML.zip
ExportFormat: html
Processors:
  -
    Executable: Snap2HTML/Snap2HTML.exe
    CommandLine: -path:%sourceDirectory% -outfile:%destinationDirectory%/Kape_Processed.html -title:"KAPE Processed Directories" -hidden -system
    ExportFormat: html

# Documentation
# https://www.rlvision.com/snap2html/about.php
# Module uses Snap2HTML to export a browseable HTML directory.
# Software author: RL Vision (Snap2HTML)
# Options available: -hidden (Include hidden files) | -system (Include system files) | -title (title of HTML file) | -link (link to path)
# HTML located at Snap2HTML/template.html can be customized.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
