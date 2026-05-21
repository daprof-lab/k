# ⚙️ **Universal Browser Parser**
### `File Name: BrowserParser.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Sebastian Søgaard  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracting browsing histories, cookies, bookmarks, and downloads from all major browsers to CSV/JSON.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Universal Browser Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Universal Browser Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Universal Browser Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Parse most artifacts in a browser to CSV or JSON
Category: WebBrowsers
Author: Sebastian Søgaard
Version: 1.0
Id: c91c1c99-f979-4c68-bcad-57f1a4afc878
BinaryUrl: https://github.com/seba7236/BrowserParser/releases/
ExportFormat: csv
Processors:
    -
        Executable: Browserparser\browserparser.exe
        CommandLine: --csv %sourceDirectory% %destinationDirectory%
        ExportFormat: csv
    -
        Executable: Browserparser\browserparser.exe
        CommandLine: --json %sourceDirectory% %destinationDirectory%
        ExportFormat: json

# Documentation
# Parses Cookies, Downloads, Favicons, History, Searches, Shortcuts and Visited Links from Chromium-based browsers
# Parses Bookmarks, Cookies, Downloads, Extensions, Favicons, Notifications, Form history, History, Inputhistory, Logins, metadata and permissions from Firefox browsers
# More artifacts may be added in the future
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
