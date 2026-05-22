# ⚙️ **Nir Soft Web Browser Downloads**
### `File Name: NirSoft_WebBrowserDownloads.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Pedro Sanchez Cordero (conexioninversa), Thomas DIOT (Qazeer)  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_WebBrowserDownloads- Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Web Browser Downloads to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Web Browser Downloads logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Web Browser Downloads timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_WebBrowserDownloads- Nirsoft'
Category: WebBrowsers
Author: Pedro Sanchez Cordero (conexioninversa), Thomas DIOT (Qazeer)
Version: 1.2
Id: 03f66bb3-0583-4371-a817-b39d9a2e4990
BinaryUrl: https://www.nirsoft.net/utils/browserdownloadsview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: BrowserDownloadsView.exe
        CommandLine: /DownloadsSource 3 /SourceFolder %sourceDirectory%\Users /ShowTimeInGMT 1 /scomma %destinationDirectory%\BrowserDownloadsView.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/web_browser_downloads_view.html
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
