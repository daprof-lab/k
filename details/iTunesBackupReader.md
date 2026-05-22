# ⚙️ **I Tunes Backup Reader**
### `File Name: iTunesBackupReader.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Jack Farley  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
iTunes Backup Reader

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run I Tunes Backup Reader to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw I Tunes Backup Reader logs to index file anomalies.
* **Incident Impact Assessment**: Leverage I Tunes Backup Reader timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'iTunes Backup Reader'
Category: ExternalDevices
Author: Jack Farley
Version: 1.0
Id: e2dbd037-69b5-476a-bbc6-9bcb737d76d4
BinaryUrl: https://github.com/jfarley248/iTunes_Backup_Analyzer/releases
ExportFormat: db
Processors:
    -
        Executable: iTunes_Backup_Reader.exe
        CommandLine: -i "%sourceDirectory%\" -o %destinationDirectory% -v --ir -r -t db
        ExportFormat: db

# Documentation
# https://github.com/jfarley248/iTunes_Backup_Reader
# Make sure to use flag --tdd false to not dedupe files (Thanks Eric!)
# Backups located in C:\Users\{user}\AppData\Roaming\Apple Computer\MobileSync\Backup\{GUID}
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
