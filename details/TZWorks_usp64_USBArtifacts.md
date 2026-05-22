# ⚙️ **Tzworks Usp64 Usbartifacts**
### `File Name: TZWorks_usp64_USBArtifacts.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Ajith Ravindran  
**Version:** 0.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Using usp64.exe to parse various artifacts generated on a Windows host whenever a plug and play device is connected on to the host.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Tzworks Usp64 Usbartifacts to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Tzworks Usp64 Usbartifacts logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Tzworks Usp64 Usbartifacts timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Using usp64.exe to parse various artifacts generated on a Windows host whenever a plug and play device is connected on to the host.'
Category: USB_Usage
Author: Ajith Ravindran
Version: 0.1
Id: cda733f0-7bd1-4fec-81a5-330d179a0d01
BinaryUrl: https://tzworks.com/prototype_page.php?proto_id=13
ExportFormat: csv
Processors:
    -
        Executable: usp64.exe
        CommandLine: -csv -dateformat dd-mm-yyyy -pair_datetime -no_whitespace -enumdir %sourceDirectory% -num_subdirs 4 -filter "setupapi.dev.log|SYSTEM|SOFTWARE|NTUSER.DAT|system.evtx|Microsoft-Windows-DriverFrameworks-UserMode%4Operational.evtx|Microsoft-Windows-Kernel-PnP%4Configuration.evtx|Microsoft-Windows-Partition%4Diagnostic.evtx"
        ExportFormat: csv
        ExportFile: USBArtifacts_Parsed.csv
        Append: true

# Documentation
# N/A
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
