# 🎯 **Frost Wire**
### `File Name: FrostWire.tkape`

{% hint style="info" %}
**Category:** Network & Web Browsers  
**Author:** Andrew Rathbun  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
FrostWire

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Frost Wire to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Frost Wire events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Frost Wire storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: FrostWire
Author: Andrew Rathbun
Version: 1.0
Id: 7e78190f-e21e-4d55-ae8a-a84e130fb1b1
RecreateDirectories: true
Targets:
    -
        Name: FrostWire Downloads
        Category: FileDownload
        Path: C:\Users\%user%\Documents\FrostWire\Torrent Data
        Recursive: true
        Comment: "Locates files downloaded that land in the default location as specified by FrostWire"
    -
        Name: FrostWire AppData
        Category: FileDownload
        Path: C:\Users\%user%\.frostwire5
        FileMask: 'frostwire.props'
        Comment: "Locates a file that contains important information about the instance of FrostWire on the user's system"
    -
        Name: FrostWire AppData
        Category: FileDownload
        Path: C:\Users\%user%\.frostwire5
        FileMask: 'itunes.props'
        Comment: "Locates a file that contains important information about the instance of FrostWire on the user's system"

# Documentation
# https://www.cyberagentsinc.com/2017/08/10/frostwire-artifacts/
# FrostWire is a Cloud Downloader, BitTorrent Client, and Media Player that's free to download and use.
# Despite warnings during install to not perform copyright infringement, this program is used for exactly that, as well as sharing other contraband.
# The above location is simply the default. The user can change this in the settings.
# FrostWire.props contains the following important values: DEFAULT_TORRENT_DATA_DIR_SETTING=, TORRENTS_DIR_SETTING=, and DIRECTORIES_TO_INCLUDE_FOR_FILES=.
# iTunes.prop contains information regarding what files are being shared by the user with the following value: IMPORT_FILES=.
# Please note: the AppData-related information doesn't populate until after the program is exited the first time after its installed by the user.
```
---

[⬅️ Back to Network & Web Browsers Targets](../network_browsers_targets.md)
