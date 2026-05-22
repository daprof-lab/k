# 🎯 **Usbdevices Logs 279b043d 4edf 40a4 A77a Cdb3f6ab37f5**
### `File Name: USBDevicesLogs_279b043d-4edf-40a4-a77a-cdb3f6ab37f5.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
USB devices log files

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Usbdevices Logs 279b043d 4edf 40a4 A77a Cdb3f6ab37f5 to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Usbdevices Logs 279b043d 4edf 40a4 A77a Cdb3f6ab37f5 events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Usbdevices Logs 279b043d 4edf 40a4 A77a Cdb3f6ab37f5 storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: USB devices log files
Author: Eric Zimmerman
Version: 1.0
Id: 07ee308f-c79a-47de-a431-c93ab34e4b66
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
        FileMask: setupapi.dev.log
    -
        Name: Setupapi.log Win7+
        Category: USBDevices
        Path: C:\Windows.old\Windows\inf\
        FileMask: setupapi.dev.log

# Documentation
# https://www.andreafortuna.org/2018/02/09/usb-devices-in-windows-forensic-analysis/
# https://www.hecfblog.com/2013/08/daily-blog-66-understanding-artifacts.html
# https://www.swiftforensics.com/2012/08/tracking-usb-first-insertion-in-event.html
# https://www.13cubed.com/downloads/dfir_cheat_sheet.pdf
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
