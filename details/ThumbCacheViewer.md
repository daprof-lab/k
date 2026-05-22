# ⚙️ **Thumb Cache Viewer**
### `File Name: ThumbCacheViewer.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Dennis Reneau, Kevin Pagano  
**Version:** 2.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
thumbcache_viewer_cmd.exe: process Windows Thumbcache files

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Thumb Cache Viewer to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Thumb Cache Viewer logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Thumb Cache Viewer timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'thumbcache_viewer_cmd.exe: process Windows Thumbcache files'
Category: FileKnowledge
Author: Dennis Reneau, Kevin Pagano
Version: 2.0
Id: 8896483c-563a-4a28-ad8a-07ba74a54a63
BinaryUrl: https://github.com/thumbcacheviewer/thumbcacheviewer/releases/download/v1.0.1.8/thumbcache_viewer_cmd.zip
ExportFormat: html
Processors:
    -
        Executable: thumbcache_viewer_cmd.exe
        CommandLine: -o %destinationDirectory%\ThumbCache_Results -w -c -z -d %sourceDirectory%
        ExportFormat: html
        ExportFile: thumbcache_results.csv

# Documentation
# Uses Thumbcache Viewer (https://github.com/thumbcacheviewer)
# Designed to work with the Thumbcache DB Target collection created by Eric Zimmerman.
# Executable author Eric Kutcher.
# Point msource (Module Source) to the Thumbcache folder or use the Target/Module option of KAPE.
# Options  -w HTML Report | -c CSV Report | -z Exclude 0 byte files | -n Prevent Thumbnail extraction | -o Output
# 2023-06-27 Updated by Kevin Pagano: Updated binary URL, changed source to directory for parsing to HMTL properly if more than DB one file
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
