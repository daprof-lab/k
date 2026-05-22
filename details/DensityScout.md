# ⚙️ **Density Scout**
### `File Name: DensityScout.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
DensityScout

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Density Scout to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Density Scout logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Density Scout timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: DensityScout
Category: FileMetadata
Author: Eric Zimmerman
Version: 1.0
Id: f93bd081-55cd-4c12-8a7f-280a0caeebf9
BinaryUrl: https://www.cert.at/media/files/downloads/software/densityscout/files/densityscout_build_45_windows.zip
ExportFormat: txt
Processors:
    -
        Executable: densityscout.exe
        CommandLine: -pe -p 0.1 -l 0.1 -d -r %sourceDirectory% -o %destinationDirectory%\DensityScout.txt
        ExportFormat: txt

# Documentation
# https://www.cert.at/en/downloads/software/software-densityscout
# https://www.sans.org/blog/finding-unknown-malware-with-densityscout/
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
