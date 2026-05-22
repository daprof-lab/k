# ⚙️ **Nir Soft Usbdeview**
### `File Name: NirSoft_USBDeview.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** NVISO (@NVISOsecurity)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
USBDeview - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Usbdeview to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Usbdeview logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Usbdeview timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'USBDeview - Nirsoft'
Category: LiveResponse
Author: NVISO (@NVISOsecurity)
Version: 1.0
Id: 9a23e756-3f18-4448-95c6-65d411f8c70b
BinaryUrl: https://www.nirsoft.net/utils/usbdeview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: usbdeview.exe
        CommandLine: /AddExportHeaderLine 1 /stab %destinationDirectory%\USBDeview.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/usb_devices_view.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
