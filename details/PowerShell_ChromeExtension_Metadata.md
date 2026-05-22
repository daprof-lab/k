# ⚙️ **Power Shell Chrome Extension Metadata**
### `File Name: PowerShell_ChromeExtension_Metadata.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Bruce Breuer  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Parse Chrome browser extension metadata from manifest.json and messages.json

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Power Shell Chrome Extension Metadata to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Power Shell Chrome Extension Metadata logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Power Shell Chrome Extension Metadata timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parse Chrome browser extension metadata from manifest.json and messages.json
Category: Browser_Extensions
Author: Bruce Breuer
Version: 1.0
Id: 7ac36894-47b7-4868-8281-95ee01a763a6
BinaryUrl: https://raw.githubusercontent.com/Reuerb/PowerShell/refs/heads/main/ChromeExtension_MetaParse.ps1
ExportFormat: csv
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: -ep bypass -Command %kapedirectory%\Modules\bin\ChromeExtension_MetaParse.ps1 -Source %sourceDirectory% | Out-File -FilePath %destinationDirectory%\ChromeExtension_Metadata.csv
        ExportFormat: csv

# Documentation
# Make sure you review, download, and place ChromeExtension_MetaParse.ps1 in the Modules\bin directory
# Runs a PowerShell script that parses the friendly name, extension ID, version, and permissions for each Chrome extension
# Use the ChromeExtension_Metadata.tkape file first to obtain the manifest/messages json files
# https://developer.chrome.com/docs/extensions/reference/manifest
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
