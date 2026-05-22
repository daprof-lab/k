# 🎯 **Scheduled Tasks**
### `File Name: ScheduledTasks.tkape`

{% hint style="info" %}
**Category:** Core OS & File System  
**Author:** Eric Zimmerman, Reece394  
**Version:** 1.2
{% endhint %}

---

## 📖 **Forensic Description & Value**
Scheduled tasks (*.job and XML)

---

## 🔍 **Investigative Use-Cases**
* **Forensic Investigation**: Extract raw records from Scheduled Tasks to uncover evidence of user interactions and operational timelines.
* **Compromise Timeline Auditing**: Correlate Scheduled Tasks events chronologically with external network indicators of compromise.
* **Data Loss & Exfiltration Review**: Audit Scheduled Tasks storage states to identify potential exfiltration triggers or local file deletions.

---

## ⚙️ **KAPE Target Definition (.tkape)**
This section shows the actual configuration of how this target is defined in KAPE:

```yaml
Description: Scheduled tasks (*.job and XML)
Author: Eric Zimmerman, Reece394
Version: 1.2
Id: e5dc4367-2e6b-49bf-a90a-d4c1598bbe28
RecreateDirectories: true
Targets:
    -
        Name: at .job
        Category: Persistence
        Path: C:\Windows\Tasks\
        FileMask: '*.job'
    -
        Name: at .job
        Category: Persistence
        Path: C:\Windows.old\Windows\Tasks\
        FileMask: '*.job'
    -
        Name: at SchedLgU.txt
        Category: Persistence
        Path: C:\Windows\
        FileMask: SchedLgU.txt
    -
        Name: at SchedLgU.txt
        Category: Persistence
        Path: C:\Windows.old\Windows\
        FileMask: SchedLgU.txt
    -
        Name: XML
        Category: Persistence
        Path: C:\Windows\System32\Tasks\
        Recursive: true
    -
        Name: XML
        Category: Persistence
        Path: C:\Windows\syswow64\Tasks\
        Recursive: true
    -
        Name: XML
        Category: Persistence
        Path: C:\Windows.old\Windows\System32\Tasks\
        Recursive: true
    -
        Name: PowerShell Scheduled_Jobs
        Category: Persistence
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\PowerShell\ScheduledJobs\
        Recursive: true
    -
        Name: PowerShell Scheduled_Jobs Output
        Category: Persistence
        Path: C:\Users\%user%\AppData\Local\Microsoft\Windows\PowerShell\ScheduledJobs\*\Output\*\
        Recursive: true
    -
        Name: PowerShell Scheduled_Jobs Systemprofile
        Category: Persistence
        Path: C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\PowerShell\ScheduledJobs\
        Recursive: true
    -
        Name: PowerShell Scheduled_Jobs Output Systemprofile
        Category: Persistence
        Path: C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\PowerShell\ScheduledJobs\*\Output\*\
        Recursive: true
    -
        Name: PowerShell Scheduled_Jobs WOW64 Systemprofile
        Category: Persistence
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Microsoft\Windows\PowerShell\ScheduledJobs\
        Recursive: true
    -
        Name: PowerShell Scheduled_Jobs Output WOW64 Systemprofile
        Category: Persistence
        Path: C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Microsoft\Windows\PowerShell\ScheduledJobs\*\Output\*\
        Recursive: true

# Documentation
# http://windowsir.blogspot.com/2009/09/parsing-job-files.html
# https://www.sans.org/blog/windows-scheduler-at-job-forensics
# https://forensicswiki.xyz/wiki/index.php?title=Windows_Job_File_Format
# https://www.forensafe.com/blogs/taskschd.html
# https://stmxcsr.com/persistence/scheduled-tasks.html
# https://www.cybertriage.com/blog/windows-scheduled-tasks-for-dfir-investigations/
# https://learn.microsoft.com/en-us/powershell/module/psscheduledjob/about/about_scheduled_jobs
# https://learn.microsoft.com/en-us/powershell/module/psscheduledjob/about/about_scheduled_jobs_troubleshooting
```
---

[⬅️ Back to Core OS & File System Targets](../core_os_artifacts_targets.md)
