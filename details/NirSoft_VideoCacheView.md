# ⚙️ **Nir Soft Video Cache View**
### `File Name: NirSoft_VideoCacheView.mkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Pedro Sanchez Cordero (conexioninversa)  
**Version:** 1.1
{% endhint %}

---

## 📖 **Forensic Description & Value**
VideoCacheView - Nirsoft

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run Nir Soft Video Cache View to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw Nir Soft Video Cache View logs to index file anomalies.
* **Incident Impact Assessment**: Leverage Nir Soft Video Cache View timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: 'VideoCacheView - Nirsoft'
Category: LiveResponse
Author: Pedro Sanchez Cordero (conexioninversa)
Version: 1.1
Id: 51c1f91a-7338-427a-9032-ec6ff08050c2
BinaryUrl: https://www.nirsoft.net/utils/videocacheview-x64.zip
ExportFormat: csv
Processors:
    -
        Executable: VideoCacheView.exe
        CommandLine: /scomma %destinationDirectory%\VideoCacheView.csv
        ExportFormat: csv

# Documentation
# After watching a video in a Web site, you may want to save the video file into your local disk for playing it offline in the future. If the video file is stored in your browser's cache, this utility can help you to extract the video file from the cache and save it for watching it in the future
# https://www.nirsoft.net/utils/video_cache_view.html
```
---

[⬅️ Back to Application Execution & Data Modules](../applications_modules.md)
