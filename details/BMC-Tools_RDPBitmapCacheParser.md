# ⚙️ **BMC RDP Cache Parser**
### `File Name: BMC-Tools_RDPBitmapCacheParser.mkape`

{% hint style="info" %}
**Category:** Cloud Storage & Remote Access  
**Author:** dingtoffee  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Decrypts and merges RDP bitmap cache tiles into complete PNG images, recreating historic remote sessions.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run BMC RDP Cache Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw BMC RDP Cache Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage BMC RDP Cache Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'BMC-Tools: RDP Bitmap Cache parser'
Category: RemoteAccess
Author: dingtoffee
Version: 1.1
Id: fcb0083d-11d7-4305-9577-2379cd243bd0
BinaryUrl: https://github.com/Qazeer/bmc-tools-compiled/releases/download/v3.02/bmc-tools.exe
FileMask: "regex:.*(.*\\.bmc|Cache.*\\.bin)$"
ExportFormat: ""
Processors:
    -
        Executable: bmc-tools.exe
        CommandLine: -s %sourceFile% -d %destinationDirectory% -b
        ExportFormat: ""

# Documentation
# https://github.com/ANSSI-FR/bmc-tools
```
---

[⬅️ Back to Cloud Storage & Remote Access Modules](../cloud_remote_modules.md)
