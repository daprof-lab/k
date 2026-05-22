# ⚙️ **Velocidex Win Pmem**
### `File Name: Velocidex_WinPmem.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Eric Capuano  
**Version:** 3.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
WinPmem Memory Dump

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Velocidex Win Pmem to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Velocidex Win Pmem logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Velocidex Win Pmem timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: WinPmem Memory Dump
Category: Memory
Author: Eric Capuano
Version: 3.0
Id: 1d284835-417b-459e-a396-d228edea3808
BinaryUrl: https://github.com/Velocidex/WinPmem/releases/download/v4.0.rc1/winpmem_mini_x64_rc2.exe
ExportFormat: raw
Processors:
    -
        Executable: winpmem.exe
        CommandLine: "%destinationDirectory%\\memory.raw"
        ExportFormat: raw

# Documentation
# https://winpmem.velocidex.com/
# https://github.com/Velocidex/WinPmem
# 1. Download winpmem_3.2.exe using the link above; also tested with winpmem_3.3.rc1.exe. Other versions may work, but are untested.
# 2. Rename the binary to winpmem.exe (dropping the version number)
# 3. Place the binary into '<KAPE_working_directory>/Modules/bin'
# KAPE should now be able to find the executable at '<KAPE_working_directory>/Modules/bin/winpmem.exe'
#
# To obtain a compressed AFF4 memory dump, swap `--format raw` for `--format map` in the command line parameter above.
#
# Example usage:
# kape.exe --tsource C --target EventLogs --tdest "C:\temp\tdest" --module WinPmem --mdest "C:\temp\mdest" --mflush --tflush
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
