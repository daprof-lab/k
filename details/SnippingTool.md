# 🎯 **Snipping Tool Screenshots**
### `File Name: SnippingTool.tkape`

{% hint style="info" %}
**Category:** Application Execution & Data  
**Author:** Paul CABON - CERT CWATCH - ALMOND  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
Cached temporary images and automatic captures from the classic Snipping Tool.

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Snipping Tool Screenshots to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Snipping Tool Screenshots events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Snipping Tool Screenshots storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: SnippingTools screenshots
Author: Paul CABON - CERT CWATCH - ALMOND
Version: 1.0
Id: 31ec21ec-f6fd-4b1f-95f7-2a2e811a241b
RecreateDirectories: true
Targets:
    -
        Name: SnippingTools screenshots in Pictures
        Category: FileKnowledge
        Path: C:\Users\*\Pictures\Screenshots\
        FileMask: '*.png'
        Comment: "Pulls all screenshots made with SnippingTool.exe"
    -
        Name: SnippingTools screenshots cached
        Category: FileKnowledge
        Path: C:\Users\*\AppData\Local\Packages\Microsoft.ScreenSketch_8wekyb3d8bbwe\TempState\Snips\
        FileMask: '*.png'
        Comment: "Pulls all temporary screenshots made with SnippingTool.exe when the save in Pictures\\Screenshots\\ is disabled. A simlar but different path used by SnipAndSketch"

# Documentation
# https://thinkdfir.com/2025/06/13/cached-screenshots-on-windows-11/
```
---

[⬅️ Back to Application Execution & Data Targets](../applications_targets.md)
