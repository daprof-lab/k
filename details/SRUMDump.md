# ⚙️ **Srumdump**
### `File Name: SRUMDump.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Brian Maloney, Jay Houlden, Vito Alfano  
**Version:** 1.3
{% endhint %}

---

## 📖 **Forensic Description & Value**
SRUM-dump: Dump contents of the SRUM database

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Srumdump to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Srumdump logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Srumdump timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'SRUM-dump: Dump contents of the SRUM database'
Category: SystemActivity
Author: Brian Maloney, Jay Houlden, Vito Alfano
Version: 1.3
Id: 74ee622c-2fb2-11ee-be56-0242ac120002
BinaryUrl: https://github.com/MarkBaggett/srum-dump/releases/download/2.6/srum_dump2.6.exe
ExportFormat: xlsx
Processors:
    -
        Executable: srum_dump.exe
        CommandLine: --SRUM_INFILE %sourceDirectory%\Windows\System32\sru\SRUDB.dat --XLSX_OUTFILE %destinationDirectory%\srum_dump_result.xlsx  --XLSX_TEMPLATE SRUM_TEMPLATE3.xlsx --REG_HIVE %sourceDirectory%\Windows\System32\config\SOFTWARE --quiet
        ExportFormat: xlsx

# Documentation
# https://github.com/MarkBaggett/srum-dump
# https://www.youtube.com/watch?v=EaEo2vnY6Aw
# https://www.youtube.com/watch?v=Uw8n4_o-ETM
# Uses new version Mark Baggett's srum-dump
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
