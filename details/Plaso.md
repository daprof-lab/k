# ⚙️ **Plaso**
### `File Name: Plaso.mkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Mark Hallman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
plaso end to end test

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Plaso to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Plaso logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Plaso timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: plaso end to end test
Category: Timeline
Author: Mark Hallman
Version: 1.0
Id: b9f74cd7-b80d-4a5c-8381-6e260ffffdf5
BinaryUrl: https://github.com/log2timeline/plaso/releases
ExportFormat: csv
Processors:
    -
        Executable: psteal.exe
        CommandLine: -z "UTC" --status_view none --source %sourceDirectory% -o l2tcsv -w %destinationDirectory%\timeline.csv
        ExportFormat: csv

# Documentation
# https://plaso.readthedocs.io/en/latest/sources/user/Using-psteal.html
# The Plaso executables are accessed via a symbolic link from the kape/bin folder to the plaso folder.
# mklink /D <kape/plaso folder> <path to plaso dir>
# Example: mklink /D C:\KAPE\Modules\bin\Plaso C:\plaso
#
# This module runs against a forensic image (E01, dd) or a folder structure.  Most common use will be
# against a folder structure. vhdx and vhd files will need to be mounted before running this module
# against them. Using this module in end to end processing
# with Kape you can't use the "--vhdx or --vhd" options.
#
# Example Kape command line: C:\kape.exe --msource E:\C\Users\ --module plaso --mdest g:\cases\sample
```
---

[⬅️ Back to Core OS & File System Modules](../core_os_artifacts_modules.md)
