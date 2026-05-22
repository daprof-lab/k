# ⚙️ **Log Parser Smbserver Anonymous Logons**
### `File Name: LogParser_SMBServerAnonymousLogons.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Hadar Yudovich, Thomas DIOT (Qazeer)  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
LogParser Microsoft-Windows-SMBServer-Security event 551

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Log Parser Smbserver Anonymous Logons to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Log Parser Smbserver Anonymous Logons logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Log Parser Smbserver Anonymous Logons timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: LogParser Microsoft-Windows-SMBServer-Security event 551
Category: RemoteAccess
Author: Hadar Yudovich, Thomas DIOT (Qazeer)
Version: 1.1
Id: 7f4fed47-cd92-4a94-a2c0-b937ea218bc8
BinaryUrl: https://www.microsoft.com/en-us/download/confirmation.aspx?id=24659
ExportFormat: csv
FileMask: Microsoft-Windows-SMBServer*Security.evtx
Processors:
    -
        Executable: LogParser.exe
        CommandLine: -stats:OFF -i:EVT "SELECT TO_UTCTIME(TimeGenerated) AS Date, EventID, 'Client attempted to access SMB via an anonymous logon.' AS Description, EXTRACT_TOKEN(Strings,8,'|') AS UserName,  EXTRACT_TOKEN(Strings,10,'|') AS ClientName INTO '%destinationDirectory%\logparser-SMBServer-Anonymous-Logon.csv' FROM '%sourceFile%' WHERE EventID=551" -filemode:0
        ExportFormat: csv

# Documentation
# Uses Microsoft Log Parser
# https://www.microsoft.com/en-us/download/confirmation.aspx?id=24659
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
