# ⚙️ **Windows Routing Table**
### `File Name: Windows_RoutingTable.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
RoutingTable

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Windows Routing Table to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Windows Routing Table logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Windows Routing Table timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: RoutingTable
Category: LiveResponse
Author: Mike Cary
Version: 1.0
Id: 8aaad838-be9e-43d4-8643-145ceaa4208b
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\route.exe
        CommandLine: print
        ExportFormat: txt
        ExportFile: routing_table.txt

# Documentation
# https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/route_ws2008
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
