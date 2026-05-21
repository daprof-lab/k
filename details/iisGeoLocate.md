# ⚙️ **IIS GeoLocate Parser**
### `File Name: iisGeoLocate.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Scans IIS log files, extracting remote IP addresses and performing geolocations.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run IIS GeoLocate Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw IIS GeoLocate Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage IIS GeoLocate Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: iisGeoLocate - Geolocate IP addresses found in IIS logs, extracts unique IPs, records bad data from logs
Category: IISLogs
Author: Andrew Rathbun
Version: 1.0
Id: beec158e-bd05-4b9f-b8dc-a99b2881b051
BinaryUrl: https://download.ericzimmermanstools.com/iisGeolocate.zip
ExportFormat: csv
Processors:
    -
        Executable: iisGeolocate\iisGeolocate.exe
        CommandLine: -d %sourceDirectory% --csv %destinationDirectory%
        ExportFormat: csv

# Documentation
# https://github.com/EricZimmerman/iisGeolocate
# https://leanpub.com/eztoolsmanuals
# Make sure you have these files in the following locations:
# .\KAPE\Modules\bin\iisGeolocate\GeoLite2-City.mmdb
# .\KAPE\Modules\bin\iisGeolocate\iisGeolocate.exe
# If you've modified KAPE to utilize the .NET 6 version of this tool, you'll need this setup:
# .\KAPE\Modules\bin\iisGeolocate\GeoLite2-City.mmdb
# .\KAPE\Modules\bin\iisGeolocate\iisGeolocate.dll
# .\KAPE\Modules\bin\iisGeolocate\iisGeolocate.exe
# .\KAPE\Modules\bin\iisGeolocate\iisGeolocate.runtimeconfig.json
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
