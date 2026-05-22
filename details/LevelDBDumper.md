# ⚙️ **Level Dbdumper**
### `File Name: LevelDBDumper.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** Matt Dawson  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Dumps LevelDB Key/Value databases

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Level Dbdumper to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Level Dbdumper logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Level Dbdumper timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: Dumps LevelDB Key/Value databases
Category: Databases
Author: Matt Dawson
Version: 1.1
Id: 3a88b531-705b-487d-933c-75ce0921a656
BinaryUrl: https://github.com/mdawsonuk/LevelDBDumper/releases
ExportFormat: csv
Processors:
    -
        Executable: LevelDBDumper.exe
        CommandLine: "-d %sourceDirectory% -o %destinationDirectory% -t csv -q --no-header --no-colour"
        ExportFormat: csv
        ExportFile: "LevelDBDumperOutput.log"
    -
        Executable: LevelDBDumper.exe
        CommandLine: "-d %sourceDirectory% -o %destinationDirectory% -t json -q --no-header --no-colour"
        ExportFormat: json
        ExportFile: "LevelDBDumperOutput.log"

# Documentation
# https://github.com/mdawsonuk/LevelDBDumper
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
