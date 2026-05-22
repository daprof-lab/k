# ⚙️ **Log Parser Detailed Network Share Access**
### `File Name: LogParser_DetailedNetworkShareAccess.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Brian Maloney/@sbousseaden  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
LogParser Security event 5145

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Log Parser Detailed Network Share Access to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Log Parser Detailed Network Share Access logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Log Parser Detailed Network Share Access timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: LogParser Security event 5145
Category: RemoteAccess
Author: Brian Maloney/@sbousseaden
Version: 1.0
Id: 2d3f0292-d302-4d4a-b292-f8fbd58b8498
BinaryUrl: https://www.microsoft.com/en-us/download/confirmation.aspx?id=24659
ExportFormat: csv
FileMask: Security.evtx
Processors:
    -
        Executable: LogParser.exe
        CommandLine: -stats:OFF -i:EVT -o CSV "SELECT TO_UTCTIME(TimeGenerated) AS Date, EventID, 'A network share object was checked to see whether client can be granted desired access.' AS Description, EXTRACT_TOKEN(Strings,1,'|') AS Username, EXTRACT_TOKEN(Strings,2,'|') AS Domain, EXTRACT_TOKEN(Strings,3,'|') AS LogonID, EXTRACT_TOKEN(Strings,5,'|') AS SourceIP, EXTRACT_TOKEN(Strings,7,'|') AS SharePath, EXTRACT_TOKEN(Strings,9,'|') AS RelativeTargetFileName, REPLACE_CHR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(REPLACE_STR(EXTRACT_TOKEN(Strings,11,'|'),'%%1537\u000D\u000A','DELETE, '),'%%1538\u000D\u000A','READ_CONTROL, '),'%%1539\u000D\u000A','WRITE_DAC, '),'%%1540\u000D\u000A','WRITE_OWNER, '),'%%1541\u000D\u000A','SYNCHRONIZE, '),'%%1542\u000D\u000A','ACCESS_SYS_SEC, '),'%%4416\u000D\u000A','ReadData (or ListDirectory), '),'%%4417\u000D\u000A','WriteData (or AddFile), '),'%%4418\u000D\u000A','AppendData (or AddSubdirectory or CreatePipeInstance), '),'%%4419\u000D\u000A','ReadEA, '),'%%4420\u000D\u000A','WriteEA, '),'%%4421\u000D\u000A','Execute (or Traverse), '),'%%4422\u000D\u000A','DeleteChild, '),'%%4423\u000D\u000A','ReadAttributes, '),'%%4424\u000D\u000A','WriteAttributes, '),'\u0009','') AS Accesses INTO '%destinationDirectory%\logparser-Network-Share-Access.csv' FROM '%sourceFile%' WHERE eventid=5145" -filemode:0
        ExportFormat: csv

# Documentation
# https://www.microsoft.com/en-us/download/details.aspx?id=24659
# https://www.stevebunting.org/udpd4n6/forensics/logparser.htm
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
