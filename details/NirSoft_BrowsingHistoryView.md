# ⚙️ **NirSoft Browsing Timeline**
### `File Name: NirSoft_BrowsingHistoryView.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Mike Cary  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Restructures historical records from all web browsers into a single chronologically sorted CSV.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run NirSoft Browsing Timeline to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw NirSoft Browsing Timeline logs to index file anomalies.
* **Incident Impact Assessment**: Leverage NirSoft Browsing Timeline timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'Browsing History View - Nirsoft'
Category: WebBrowsers
Author: Mike Cary
Version: 1.1
Id: 53d5bea2-b3d3-4a60-8844-be898390adc1
BinaryUrl: https://www.nirsoft.net/utils/browsinghistoryview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: browsinghistoryview.exe
        CommandLine: /HistorySource 3 /HistorySourceFolder %sourceDirectory%\Users /VisitTimeFilterType 1 /ShowTimeInGMT 1 /scomma %destinationDirectory%\BrowsingHistory.csv
        ExportFormat: csv
        ExportFile: NirSoftBrowsingHistoryViewConsoleOutput.txt
    -
        Executable: browsinghistoryview.exe
        CommandLine: /HistorySource 3 /HistorySourceFolder %sourceDirectory%\Users /VisitTimeFilterType 1 /ShowTimeInGMT 1 /sverhtml  %destinationDirectory%\BrowsingHistory.html
        ExportFormat: html
        ExportFile: NirSoftBrowsingHistoryViewConsoleOutput.txt

# Documentation
# Uses Nirsoft's BrowsingHistoryView to export browsing history for all users to CSV
# https://www.nirsoft.net/utils/browsing_history_view.html
# ***Must set msource to users directory of triage to be parsed***
# Example: .\kape.exe --msource G:\Kape_TEST\C\Users --mdest D:\Kape_moduleOut --module BrowsingHistoryView
# Example: .\kape.exe --msource G:\Kape_TEST\VSS21\Users --mdest D:\Kape_moduleOut --module BrowsingHistoryView
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
