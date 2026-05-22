# ⚙️ **Thor Lite Live Response Lookback30days**
### `File Name: Thor-Lite_LiveResponse_Lookback30days.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Thor Lite, an IOC and YARA scanner written in Golang with 30 Days lookback option

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Thor Lite Live Response Lookback30days to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Thor Lite Live Response Lookback30days logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Thor Lite Live Response Lookback30days timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Thor Lite, an IOC and YARA scanner written in Golang with 30 Days lookback option
Category: IOCs
Author: Georg Lauenstein
Version: 1.0
Id: 5dafe1af-eb44-4b08-a7fd-8e36d65d6a60
BinaryUrl: https://www.nextron-systems.com/thor-lite/
ExportFormat: csv
Processors:
    -
        Executable: thor-lite\thor64-lite.exe
        CommandLine: "--quick --nothordb --processintegrity --lookback 30 --showdeleted -o :hostname:\_:time:.csv -e %destinationDirectory%\\THOR"
        ExportFormat: csv

# Documentation
# HOW TO PLACE THE BINARY
# 1. Download thor-lite using the link above. It's a free tool, but you must register for a license.
# 2. Unzip thor-lite.zip into '<KAPE_working_directory>\Modules\bin\thor-lite'
# 3. Rename the unpacked 'thor-lite-win-pack' directory to 'thor-lite'
# 4. Update the yara signatures -> '.\thor-lite-util.exe update'
# 5. KAPE should now be able to find the executable in '<KAPE_working_directory>/Modules/bin/thor-lite/thor64-lite.exe'
# 6. Be sure to include your '.lic' license file in the 'thor-lite'
# 7. For more options check: https://thor-manual.nextron-systems.com/en/latest/index.html
#
# Currently configured to run "--quick" option which "selects the most relevant file paths only"
# Remove "--quick" for a full scan which will take much longer. (~2min versus 23min on test system)
# for Filescan use "Thor-Lite_Scan.mkape"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
