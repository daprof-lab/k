# ⚙️ **Nirsoft Wireless Key View**
### `File Name: Nirsoft_WirelessKeyView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NirSoft_WirelessKeyView - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Wireless Key View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Wireless Key View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Wireless Key View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'NirSoft_WirelessKeyView - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: f1fecc82-8f11-4dc8-be5f-9af2c4d63ef6
BinaryUrl: https://www.nirsoft.net/toolsdownload/wirelesskeyview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: WirelessKeyView.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_WirelessKeyView.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/wireless_key.html
# WirelessKeyView recovers all wireless network security keys/passwords (WEP/WPA) stored in your computer by the 'Wireless Zero Configuration' service of Windows XP or by the 'WLAN AutoConfig' service of Windows Vista, Windows 7, Windows 8, Windows 10, and Windows Server 2008. It allows you to easily save all keys to text/html/xml file, or copy a single key to the clipboard. You can also export your wireless keys into a file and import these keys into another computer.
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
