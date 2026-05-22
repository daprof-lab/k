# ⚙️ **Nirsoft Bluetooth View**
### `File Name: Nirsoft_BluetoothView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_BluetoothView - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Bluetooth View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Bluetooth View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Bluetooth View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_BluetoothView - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: e1816e7e-ff9b-430c-8650-b5650f68028b
BinaryUrl: https://www.nirsoft.net/utils/bluetoothview.zip
ExportFormat: txt
Processors:
    -
        Executable: BluetoothView.exe
        CommandLine: /stext %destinationDirectory%\Nirsoft_BluetoothView.txt
        ExportFormat: txt

# Documentation
# https://www.nirsoft.net/utils/bluetooth_viewer.html
# BluetoothView is a small utility that runs in the background, and monitor the activity of Bluetooth devices around you. For each detected Bluetooth device, it displays the following information: Device Name, Bluetooth Address, Major Device Type, Minor Device Type, First Detection Time, Last Detection Time, and more.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
