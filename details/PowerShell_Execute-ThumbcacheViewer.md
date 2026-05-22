# ⚙️ **Power Shell Execute Thumbcache Viewer**
### `File Name: PowerShell_Execute-ThumbcacheViewer.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Thomas DIOT (Qazeer)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Execute-ThumbcacheViewer.ps1 - Recursively process the source directory to execute thumbcache_viewer_cmd.exe over each thumbcache subfolder(s) found.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Execute Thumbcache Viewer to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Execute Thumbcache Viewer logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Execute Thumbcache Viewer timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Execute-ThumbcacheViewer.ps1 - Recursively process the source directory to execute thumbcache_viewer_cmd.exe over each thumbcache subfolder(s) found.
Category: FileKnowledge
Author: Thomas DIOT (Qazeer)
Version: 1.0
Id: c53c0e53-8c81-4e03-8140-890c745142b0
BinaryUrl: https://gist.github.com/Qazeer/cb3a0cf306bc1f75a2d5a8cef5b9ffa9
ExportFormat: CSV
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: "& '%kapeDirectory%\\Modules\\bin\\Execute-ThumbcacheViewer.ps1' -thumbcacheViewerBinary '%kapeDirectory%\\Modules\\bin\\thumbcache_viewer_cmd.exe' -InputDir '%sourceDirectory%' -OutputDir %destinationDirectory%"
        ExportFormat: CSV

# Documentation
# Recursively process the source directory to execute thumbcache_viewer_cmd.exe over each thumbcache subfolder(s) found.
# Execute-ThumbcacheViewer.ps1 is basically a wrapper to make thumbcache_viewer_cmd.exe recursive, as the tool can natively only process a thumbcache subfolder
# and not multiple thumbcache subfolder(s) from the drive root or user profile folders.
# https://gist.github.com/Qazeer/cb3a0cf306bc1f75a2d5a8cef5b9ffa9
# thumbcache_viewer_cmd.exe (https://github.com/thumbcacheviewer/thumbcacheviewer/releases/download/v1.0.1.8/thumbcache_viewer_cmd.zip) must be placed under "%kapeDirectory%\Modules\bin\thumbcache_viewer_cmd.exe".
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
