# ⚙️ **NTLM Hash Dumper**
### `File Name: NTLM_Hash_Dumper.mkape`

{% hint style="info" %}
**Category:** Memory & Virtualization  
**Author:** DReneau  
**Version:** 1.0
{% endhint %}

---

## 📖 **Forensic Description & Value**
NTLM Hash Dumper | NTLMv1/2

---

## 🔍 **Investigative Use-Cases**
* **Bulk Automated Parsing**: Run NTLM Hash Dumper to parse multiple folders containing acquired target evidence in a single instruction.
* **Structured Report Output**: Generate sorted, structured CSV/JSON databases from raw NTLM Hash Dumper logs to index file anomalies.
* **Incident Impact Assessment**: Leverage NTLM Hash Dumper timeline outputs to isolate exactly when unauthorized scripts were loaded.

---

## ⚙️ **KAPE Module Definition (.mkape)**
This section shows the actual configuration of how this module is defined in KAPE:

```yaml
Description: NTLM Hash Dumper | NTLMv1/2
Category: Passwords
Author: DReneau
Version: 1.0
Id: fc897d04-9ec1-472c-97cd-f99feb39bbe9
BinaryUrl: https://github.com/Retr0-code/hash-dumper/releases/download/v1.0.4/hash_dumper_v1.0.4_win64.zip
ExportFormat: txt
Processors:
    -
        Executable: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        CommandLine: |
            $systemFile = Get-ChildItem -Path '%sourceDirectory%' -Filter 'SYSTEM' -Recurse | Select-Object -First 1;
            $samFile = Get-ChildItem -Path '%sourceDirectory%' -Filter 'SAM' -Recurse | Select-Object -First 1;

            if ($systemFile -and $samFile) {
                & '%kapedirectory%\Modules\bin\hash_dumper.exe' --system $systemFile.FullName --sam $samFile.FullName;
                Start-Sleep -Seconds 2;
                $maxRetries = 3;
                $retryCount = 0;
                while ($retryCount -lt $maxRetries) {
                    try {
                        Out-File -FilePath '%destinationDirectory%\dumped_NTLM_hashes.txt' -Encoding utf8 -Append;
                        break;
                    } catch {
                        Start-Sleep -Seconds 2;
                        $retryCount++;
                    }
                }
            } else {
                Write-Host 'SAM or SYSTEM files not found.'
            }
        ExportFormat: txt
        ExportFile: dumped_NTLM_hashes.txt

# Documentation
# https://github.com/Retr0-code/hash-dumper
# This module extracts the Windows NTLM hashes for every user account. 
# Point the 'module source' to the acquired "\Windows\System32\config" folder
# Place the " hash_dumper_v1.0.4_win64.zip " archive into "Modules\bin" and extract hash_dumper.exe.
# Remember: NTLM-hash 31d6cfe0d16ae931b73c59d7e0c089c0 means "blank"
#
# Windows NTLM hash dump utility written in C language, that supports Windows and Linux. Hashes can be dumped in realtime or from already saved SAM and SYSTEM hives.
#
# Example:
# .\kape.exe --msource C:\kape\path\to\acquired\Windows\System32\config --mdest C:\kape\out --module ntlm_hash_dumper
```
---

[⬅️ Back to Memory & Virtualization Modules](../memory_virtualization_modules.md)
