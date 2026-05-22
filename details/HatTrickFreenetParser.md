# ⚙️ **Hat Trick Freenet Parser**
### `File Name: HatTrickFreenetParser.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Charlie Rubisoff  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Hat-Trick: Freenet Parser

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Hat Trick Freenet Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Hat Trick Freenet Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Hat Trick Freenet Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Hat-Trick: Freenet Parser'
Category: Misc
Author: Charlie Rubisoff
Version: 1.0
Id: 5c546be1-27f9-4739-86f6-e0391d1cc7db
BinaryUrl: https://github.com/northloopforensics/Hat-Trick-Freenet-Parser/releases
ExportFormat: txt
Processors:
    -
        Executable: Hat-Trick.Freenet.Parser.exe
        CommandLine: "%sourceDirectory% %destinationDirectory%"
        ExportFormat: txt

# Documentation
# https://github.com/northloopforensics/Hat-Trick-Freenet-Parser
# Executable to parse Freenet installations using KAPE
# This program was written for use on Kroll's KAPE tool. Download the release and then copy the #executable to: kape\Modules\bin
# Also available in this repository are the Target profile (tkape) file and Module profile #(mkape) file. Copy these to the appropriate locations: kape\Targets\P2P\freenet.tkape & #kape\Modules\Misc\hat-trick-freenet-parser.mkape
# The tool parses: The Location ID and Network Addresses of the Target System Downloaded and #Uploaded File Information Peer IDs, Peer IP Addresses, and Peer-of-Peer Location IDs
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
