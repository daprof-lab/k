# ⚙️ **Belkasoft RAM Capture**
### `File Name: Belkasoft_RAMCapture.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Nick Polosukhin  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Lightweight, kernel-safe tool to obtain physical memory snapshots.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Belkasoft RAM Capture to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Belkasoft RAM Capture logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Belkasoft RAM Capture timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Belkasoft RAM Capture Memory Acquisition
Category: Memory
Author: Nick Polosukhin
Version: 1.0
Id: b1da512a-a11a-4d2d-8361-0344acaf1dd7
BinaryUrl: https://belkasoft.com/ram-capturer
ExportFormat: raw
Processors:
  -
    Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
    CommandLine: -Command "$arch = if ([Environment]::Is64BitOperatingSystem) { 'x64' } else { 'x86' };$hostname=$env:COMPUTERNAME;$dumpname=$hostname+'-RAM.raw';$dumppath = Join-Path -Path %destinationDirectory% -ChildPath $dumpname;$toolPath = Join-Path -Path '%kapedirectory%\Modules\bin\BelkaSoft' -ChildPath $arch; $exe = Join-Path $toolPath 'RamCapture.exe'; Start-Process -FilePath $exe -ArgumentList $dumppath -Wait"
    ExportFormat: raw

# Documentation
# https://belkasoft.com/ram-capturer
#
# 1. Download Belkasoft RAM Capture (Module works with both x86 and x64 binaries). The folder structure is taken from https://github.com/mikebdp2/ram-capturer/tree/master
# 2. Rename both binaries to RamCapture.exe
# 3. Place folders x86 and x64 into '<KAPE_working_directory>/Modules/bin/BelkaSoft'
# Module dynamically determines OS arch with PowerShell and launches the proper version of RAMCapture.
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
