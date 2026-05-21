# **🌐 Network & Web Browsers**

{% hint style="info" %}

**Investigator Note:** Targets and Modules related to browser history, downloads, extensions, as well as core OS networking artifacts (ARP cache, DNS cache, routing tables, and IIS/Apache logs).

{% endhint %}

---

## **Explore Category Contents**

Select a sub-page below to browse the full forensic components in this category.

### 🎯 [Browse Targets (.tkape)](network_browsers_targets.md)
> Collect raw forensic artifacts from web browsers and operating system network status.
> * **16 Targets Available** (e.g., `Chrome.tkape`, `Firefox.tkape`, `Windows_IPConfig.mkape`)
> * [View All Targets &rarr;](network_browsers_targets.md)

### ⚙️ [Browse Modules (.mkape)](network_browsers_modules.md)
> Process browser histories and network logs to extract URLs, caches, credentials, and access requests.
> * **8 Modules Available** (e.g., `BrowserParser.mkape`, `NirSoft_BrowsingHistoryView.mkape`, `bstrings_IPv4.mkape`)
> * [View All Modules &rarr;](network_browsers_modules.md)

---

## 📊 **Category Quick Stats**

| Metric | Details |
| :--- | :--- |
| **📁 Focus Area** | Browser cache, extensions, routing tables, DNS logs, and web server access logs (IIS/Apache) |
| **🎯 Total Targets** | **16** configuration files |
| **⚙️ Total Modules** | **8** parser plugins |

---

## 💡 **Key Highlighted Artifacts**

* **Web Browsers (Chrome, Edge, Firefox, Brave, Opera, Vivaldi)**: Retrieve user searching history, file downloads, session cookies, autocomplete forms, and saved login data.
* **Browser Cache & Extensions**: Identify sideloaded browser plugins and inspect cached images or pages from web-based exfiltration.
* **OS Network Diagnostics (IPConfig, DNS, ARP, Routing)**: Map out local system networking states and discover recently queried domains.
* **Web Server Logs (IIS, Apache)**: Audit web access logs for incoming attack patterns, automated directory brute-forcing, or payload delivery.