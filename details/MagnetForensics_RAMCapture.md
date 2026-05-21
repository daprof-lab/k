# ⚙️ **Magnet RAM Capture**
### `File Name: MagnetForensics_RAMCapture.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Doug Metz  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Automated, low-overhead RAM dump utility that outputs physical memory dumps to local storage.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Magnet RAM Capture to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Magnet RAM Capture logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Magnet RAM Capture timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Magnet RAM Capture Memory Acquisition
Category: Memory
Author: Doug Metz
Version: 1.1
Id: 23a35c17-15a8-4d7e-9029-083bc70bd4ef
BinaryUrl: https://support.magnetforensics.com/
ExportFormat: raw
Processors:
    -
        Executable: MRC.exe
        CommandLine: "/accepteula /go %destinationDirectory%\\memory.raw /silent"
        ExportFormat: raw

# Documentation
# https://www.magnetforensics.com/resources/magnet-ram-capture
#
# 1. Download Magnet RAM Capture using the link above; tested with version 1.2
# 2. Rename the binary to MRC.exe
# 3. Place the binary into '<KAPE_working_directory>/Modules/bin'
# KAPE should now be able to find the executable at '<KAPE_working_directory>/Modules/bin/MRC.exe'
#
# Example usage:
# kape.exe --tsource C: --tdest E:\Triage\ --target KapeTriage --vhdx triage --mdest E:\Triage\Memory --module MagnetRamCapture
#
# Bug: Spaces in the destinationDirectory will cause MRC to fail to collect/crash.
# Workarounds include modifying this module to include the destination path manually (with quotes) or avoid spaces in the mdest parameter
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
