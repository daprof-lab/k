# ⚙️ **Magnet Forensics EDD**
### `File Name: MagnetForensics_EDD.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Mohamed El-Hadidi  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Checks the local physical drives on a system for TrueCrypt, PGP, VeraCrypt, SafeBoot, or Bitlocker encrypted volumes

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Magnet Forensics EDD to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Magnet Forensics EDD logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Magnet Forensics EDD timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Checks the local physical drives on a system for TrueCrypt, PGP, VeraCrypt, SafeBoot, or Bitlocker encrypted volumes
Category: LiveResponse
Author: Mohamed El-Hadidi
Version: 1.1
Id: c7212da1-ed41-4560-95f7-1a2d99acc1f8
BinaryUrl: https://www.magnetforensics.com/resources/encrypted-disk-detector/
ExportFormat: txt
Processors:
    -
        Executable: EDD\EDDv310.exe
        CommandLine: /batch >> %destinationDirectory%
        ExportFormat: txt
        ExportFile: EDD.txt

# Documentation
# https://www.magnetforensics.com/resources/encrypted-disk-detector/
# Create a folder "EDD" within the "Modules\bin" KAPE folder
# Place "EDDv310.exe", "EDDv310.exe.config" files into "Modules\bin\EDD"
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
