# ⚙️ **Srumdump 02d088e0 5bdc 47a7 8e6c Dc7fdc7cbb4f**
### `File Name: SRUMDump_02d088e0-5bdc-47a7-8e6c-dc7fdc7cbb4f.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Brian Maloney, Jay Houlden  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
SRUM-dump: Dump contents of the SRUM database

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Srumdump 02d088e0 5bdc 47a7 8e6c Dc7fdc7cbb4f to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Srumdump 02d088e0 5bdc 47a7 8e6c Dc7fdc7cbb4f logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Srumdump 02d088e0 5bdc 47a7 8e6c Dc7fdc7cbb4f timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'SRUM-dump: Dump contents of the SRUM database'
Category: SystemActivity
Author: Brian Maloney, Jay Houlden
Version: 1.1
Id: 8e0a2314-79e4-48f2-81ad-a0719e8af680
BinaryUrl: https://github.com/MarkBaggett/srum-dump/raw/python3/srum_dump_csv.exe
ExportFormat: csv
Processors:
    -
        Executable: srum_dump_csv.exe
        CommandLine: -i %sourceDirectory%\WINDOWS\System32\sru\SRUDB.dat -t SRUM_TEMPLATE.xlsx -r %sourceDirectory%\WINDOWS\System32\config\SOFTWARE -o %destinationDirectory% -q
        ExportFormat: csv

# Documentation
# https://github.com/MarkBaggett/srum-dump
# https://www.youtube.com/watch?v=EaEo2vnY6Aw
# https://www.youtube.com/watch?v=Uw8n4_o-ETM
# Uses Mark Baggett's srum-dump
# SRUM_TEMPLATE.xlsx should also be in KAPE\Modules\bin
# https://github.com/MarkBaggett/srum-dump/raw/python3/srum_dump_csv.exe
# ***Must set -i to srudb.dat and -r to SOFTWARE hive in CommandLine***
# Example: CommandLine: -i %sourceDirectory%\files\C\WINDOWS\System32\sru\SRUDB.dat -t SRUM_TEMPLATE.xlsx -r %sourceDirectory%\files\C\WINDOWS\System32\config\SOFTWARE -o %destinationDirectory% -q
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
