# ⚙️ **Loki IOC Scanner**
### `File Name: Loki_Scan.mkape`

{% hint style="info" %}
**Category:** Threat Hunting, AV & Logs  
**Author:** Georg Lauenstein and Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Light and fast Incident Response scanner mapping systems against public YARA and MD5 signatures.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Loki IOC Scanner to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Loki IOC Scanner logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Loki IOC Scanner timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Loki - Simple IOC and Incident Response Scanner - Mounted Image/Offline Files
Category: IOCs
Author: Georg Lauenstein and Andrew Rathbun
Version: 1.0
Id: 3c715b0c-fec3-4f41-a762-74233e240760
BinaryUrl: https://github.com/Neo23x0/Loki/releases/download/v0.44.2/loki_0.44.2.zip
ExportFormat: log
Processors:
    -
        Executable: Loki\loki.exe
        CommandLine: "-p %sourceDirectory% --noprocscan --pesieveshellc --rootkit --intense --logfolder %destinationDirectory% --debug"
        ExportFormat: log

# Documentation
# HOW TO PLACE THE BINARY
# 1. Download loki using the link above. It's a free tool
# 2. Unzip loki.zip into '<KAPE_working_directory>/Modules'
# 3. Update the yara signatures -> 'loki.exe --update'
# 4. KAPE should now be able to find the executable in '<KAPE_working_directory>/Modules/bin/loki/loki.exe'
# 5. Use 'loki.exe --help' for options
# 6. More info here: https://www.nextron-systems.com/loki/
```
---

[⬅️ Back to Threat Hunting, AV & Logs Modules](../threat_hunting_modules.md)
