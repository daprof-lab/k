# ⚙️ **Mc Afee Stinger**
### `File Name: McAfeeStinger.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Georg Lauenstein  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
McAfeeStinger scanner

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Mc Afee Stinger to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Mc Afee Stinger logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Mc Afee Stinger timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: McAfeeStinger scanner
Category: LiveResponse
Author: Georg Lauenstein
Version: 1.0
Id: c49d14fe-5b77-46d9-a058-ab90d5cc2edd
BinaryUrl: https://www.mcafee.com/enterprise/en-us/downloads/free-tools/terms-of-use.html?url=https://downloadcenter.mcafee.com/products/mcafee-avert/Stinger/stinger32.exe
ExportFormat: html
Processors:
    -
        Executable: McAfeeStinger\stinger32.exe
        CommandLine: "--SILENT --SCANPATH=%sourceDirectory% --NOREGISTRY --NOPROCESS --RPTALL --REPORTPATH= %destinationDirectory%"
        ExportFormat: html

# Documentation
# Create a folder "McAfeeStinger" within the "Modules\bin" KAPE folder
# Place "stinger32.exe" file into "Modules\bin\McAfeeStinger"
# Release Infos: https://www.mcafee.com/enterprise/de-de/downloads/free-tools/stinger.html
# Change Infos: https://downloadcenter.mcafee.com/products/mcafee-avert/stinger/readme.txt
# More Options for Commandline: https://community.mcafee.com/t5/Malware/Stinger-command-line-options-silent-log/m-p/404506/highlight/true#M30492
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
