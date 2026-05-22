# ⚙️ **Nirsoft Shadow Copy View**
### `File Name: Nirsoft_ShadowCopyView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
ShadowCopyView is simple tool for Windows 10/8/7/Vista that lists the snapshots of your hard drive created by the 'Volume Shadow Copy' service of Windows. Every snapshot contains an older versions of your files and folders from the date that the snapshot was created, you can browse the older version of your files and folders, and optionally copy them into a folder on your disk.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Shadow Copy View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Shadow Copy View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Shadow Copy View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: ShadowCopyView is simple tool for Windows 10/8/7/Vista that lists the snapshots of your hard drive created by the 'Volume Shadow Copy' service of Windows. Every snapshot contains an older versions of your files and folders from the date that the snapshot was created, you can browse the older version of your files and folders, and optionally copy them into a folder on your disk.
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: ec320e6b-3668-4cbf-9cf5-2459c74142b9
BinaryUrl: https://www.nirsoft.net/utils/shadowcopyview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: shadowcopyview.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_shadowcopyview.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/shadow_copy_view.html
# information is displayed: Filename, Threat Name, Severity, Process Name, Initial Detect Time, Status Change Time, Remediation Time, Threat ID, Threat Status, Default Threat Action, and more...
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
