# ⚙️ **Nirsoft What In Startup**
### `File Name: Nirsoft_WhatInStartup.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_WhatInStartup - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft What In Startup to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft What In Startup logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft What In Startup timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_WhatInStartup - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: a62b184e-b03f-4f77-a893-a9aded790c7b
BinaryUrl: https://www.nirsoft.net/utils/WhatInStartup.zip
ExportFormat: txt
Processors:
    -
        Executable: WhatInStartup.exe
        CommandLine: /stext %destinationDirectory%\Nirsoft_WhatInStartup.txt
        ExportFormat: txt

# Documentation
# https://www.nirsoft.net/utils/WhatInStartup.html
# This utility displays the list of all applications that are loaded automatically when Windows starts up. For each application, the following information is displayed: Startup Type (Registry/Startup Folder), Command-Line String, Product Name, File Version, Company Name, Location in the Registry or file system, and more.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
