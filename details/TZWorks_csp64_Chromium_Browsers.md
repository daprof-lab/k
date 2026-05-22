# ⚙️ **Tzworks Csp64 Chromium Browsers**
### `File Name: TZWorks_csp64_Chromium_Browsers.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using csp64.exe to parse all available artifacts from Chromium based browsers like Google Chrome. 7 databases are parsed using the tool (a) History, (b) Cookies, (c) Web Data, (d) Top Sites, (e) Shortcuts, (f) Login Data and (g) Favicons.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Csp64 Chromium Browsers to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Csp64 Chromium Browsers logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Csp64 Chromium Browsers timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using csp64.exe to parse all available artifacts from Chromium based browsers like Google Chrome. 7 databases are parsed using the tool (a) History, (b) Cookies, (c) Web Data, (d) Top Sites, (e) Shortcuts, (f) Login Data and (g) Favicons.'
Category: Browser_Artifacts
Author: Ajith Ravindran
Version: 0.1
Id: 24032121-4641-4758-b007-f10e65f5f442
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=45
FileMask: regex:(Web Data|Cookie|History|Favicons|Logins|Shortcuts|Top Sites)
ExportFormat: csv
Processors:
    -
        Executable: csp64.exe
        CommandLine: -db %sourceFile% -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace
        ExportFormat: csv
        ExportFile: Chromium_Browsers_Parsed.csv
        Append: true


# Documentation
# N/A
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
