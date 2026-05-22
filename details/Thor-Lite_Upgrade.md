# ⚙️ **Thor Lite Upgrade**
### `File Name: Thor-Lite_Upgrade.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Thor Lite, an IOC and YARA scanner written in Golang

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Thor Lite Upgrade to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Thor Lite Upgrade logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Thor Lite Upgrade timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Thor Lite, an IOC and YARA scanner written in Golang
Category: IOCs
Author: Andrew Rathbun
Version: 1.0
Id: e7ae5267-ccbc-49ae-8eaf-b6f031c750e5
BinaryUrl: https://www.nextron-systems.com/thor-lite/
ExportFormat: ""
Processors:
    -
        Executable: thor-lite\thor-lite-util.exe
        CommandLine: "upgrade"
        ExportFormat: ""

# Documentation
# HOW TO PLACE THE BINARY
# 1. Download thor-lite using the link above. It's a free tool, but you must register for a license
# 2. Unzip thor-lite.zip into '<KAPE_working_directory>\Modules\bin\thor-lite'
# 3. Rename the unpacked 'thor-lite-win-pack' directory to 'thor-lite'
# 4. Update the YARA signatures -> '.\thor-lite-util.exe update'
# 5. KAPE should now be able to find the executable in '<KAPE_working_directory>/Modules/bin/thor-lite'
# 6. Be sure to include your '.lic' license file in the 'thor-lite'
# 7. For more options check: https://thor-manual.nextron-systems.com/en/latest/index.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
