# 🎯 **USB Device Logs**
### `File Name: USBDevicesLogs.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman, esecrpm  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Collects setupapi.dev.log files, system setup logs, and hardware device logs detailing external storage connections and driver setups.

---

## 🔍 **Investigative Use-Cases**
* **Unauthorized Storage Detection**: Locate when an external USB flash drive or hard drive was first and last connected to the system.
* **Hardware Vendor Profiling**: Determine the vendor, model, serial number, and friendly name of historically inserted storage media.
* **Insider Threat Auditing**: Correlate USB device connections with large data movements or file access records.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: USB devices log files
Author: Eric Zimmerman, esecrpm
Version: 1.1
Id: 1c1d3c54-fb49-4ed1-81f7-03c6744167a1
RecreateDirectories: true
Targets:
    -
        Name: Setupapi.log XP
        Category: USBDevices
        Path: C:\Windows\
        FileMask: setupapi.log
    -
        Name: Setupapi.log Win7+
        Category: USBDevices
        Path: C:\Windows\inf\
        FileMask: setupapi.*.log
    -
        Name: Setupapi.log Win7+
        Category: USBDevices
        Path: C:\Windows.old\Windows\inf\
        FileMask: setupapi.*.log

# Documentation
# https://www.andreafortuna.org/2018/02/09/usb-devices-in-windows-forensic-analysis/
# https://www.hecfblog.com/2013/08/daily-blog-66-understanding-artifacts.html
# https://www.swiftforensics.com/2012/08/tracking-usb-first-insertion-in-event.html
# https://www.13cubed.com/downloads/dfir_cheat_sheet.pdf
#
# v1.1
# Use wildcard to account for dated versions files and other forms of setupapi log
# Ex: setupapi.dev.20221214_093731.log, setupapi.setup.log, setupapi.upgrade.log
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
