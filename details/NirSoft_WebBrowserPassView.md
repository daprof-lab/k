# ⚙️ **NirSoft WebPass Parser**
### `File Name: NirSoft_WebBrowserPassView.mkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
Extracts and decrypts saved credentials, login forms, and passwords from popular browsers.

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run NirSoft WebPass Parser to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw NirSoft WebPass Parser logs to index file anomalies.
* **Incident Impact Assessment**: Leverage NirSoft WebPass Parser timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'WebBrowserPassView - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.1
Id: a216d646-cbac-45bb-8340-e0168baac683
BinaryUrl: https://www.nirsoft.net/protected_downloads/passreccommandline.zip
ExportFormat: csv
Processors:
    -
        Executable: WebBrowserPassView.exe
        CommandLine: /scomma %destinationDirectory%\WebBrowserPassView.csv
        ExportFormat: csv

# Documentation
# WebBrowserPassView is a password recovery tool that reveals the passwords stored by the following Web browsers: Internet Explorer (Version 4.0 - 11.0), Mozilla Firefox (All Versions), Google Chrome, Safari, and Opera. This tool can be used to recover your lost/forgotten password of any Website, including popular Web sites, like Facebook, Yahoo, Google, and GMail, as long as the password is stored by your Web Browser.
# **Do not download** from the following location httpx://www.nirsoft.net/toolsdownload/webbrowserpassview.zip
# As indicated on the Nirsoft website, the options to save from the command line are disabled. You can find a package of password-recovery tools with full command-line support on the following Web page: https://www.nirsoft.net/password_recovery_tools.html
# and follow the next steps:
# 1. Click this download link. https://www.nirsoft.net/protected_downloads/passreccommandline.zip
# 2. Enter 'download' as the user name, and 'nirsoft123!' as the password.
# 3. After downloading the package, extract the files from it using the following password: nirsoft123!
# 4. Get the executable and copy it to the \Modules\Bin directory
```
---

[⬅️ Back to Network & Web Browsers Modules](../network_browsers_modules.md)
