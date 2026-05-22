# ⚙️ **Nirsoft Dnsdata View**
### `File Name: Nirsoft_DNSDataView.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
DNSDataView This utility is alternative to the NSLookup tool that comes with Windows operating system. It allows you to easily retrieve the DNS records (MX, NS, A, SOA) of the specified domains. You can use the default DNS server of your Internet connection, or use any other DNS server that you specify. After retrieving the DNS records for the desired domains

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nirsoft Dnsdata View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nirsoft Dnsdata View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nirsoft Dnsdata View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: DNSDataView This utility is alternative to the NSLookup tool that comes with Windows operating system. It allows you to easily retrieve the DNS records (MX, NS, A, SOA) of the specified domains. You can use the default DNS server of your Internet connection, or use any other DNS server that you specify. After retrieving the DNS records for the desired domains
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.0
Id: c65bf3f4-6165-4f90-a968-d02f21bcb2f4
BinaryUrl: https://www.nirsoft.net/utils/dnsdataview.zip
ExportFormat: csv
Processors:
    -
        Executable: DNSDataView.exe
        CommandLine: /scomma %destinationDirectory%\Nirsoft_DNSDataView.csv
        ExportFormat: csv

# Documentation
# https://www.nirsoft.net/utils/outlook_attachment.html
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
