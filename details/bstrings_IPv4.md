# ⚙️ **bstrings IPv4 Extractor**
### `File Name: bstrings_IPv4.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Chris Kudless, Georg Lauenstein  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Scans data using bstrings regex to locate valid IPv4 addresses.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run bstrings IPv4 Extractor to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw bstrings IPv4 Extractor logs to index file anomalies.
* **Incident Impact Assessment**: Leverage bstrings IPv4 Extractor timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Use bstrings to GREP for IPv4 addresses
Category: KeywordSearches
Author: Chris Kudless, Georg Lauenstein
Version: 1.2
Id: 86b15511-7b40-435f-a3a3-197ee32dc394
BinaryUrl: https://download.ericzimmermanstools.com/bstrings.zip
ExportFormat: txt
Processors:
    -
        Executable: bstrings.exe
        CommandLine: -d %sourceDirectory% -o '%destinationDirectory%' --lr ipv4 --ro
        ExportFormat: txt
        ExportFile: IPv4-Addresses.txt

# Documentation
# https://github.com/EricZimmerman/bstrings
# https://www.youtube.com/watch?v=GhCZfCzn2l0
# https://binaryforay.blogspot.com/search?q=bstrings
# https://www.sans.org/posters/eric-zimmerman-tools-cheat-sheet/
# https://leanpub.com/eztoolsmanuals
# Can be used to generate a single list of IP addresses from one or multiple data sources. Create a copy of the output file, open the copy in your favorite text editor, sort alphabetically, deduplicate, delete any logging data from the output, and use your favorite IP Geolocate tool to ID noteworthy IPs.
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
