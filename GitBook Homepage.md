# **🏠 Introduction to KAPE**

{% hint style="success" %}

**Welcome to the KAPE Modules and Targets Documentation.** Generated and updated for the modern DFIR investigator.

{% endhint %}

## **What is KAPE?**

Kroll Artifact Parser and Extractor (KAPE) is an incredibly powerful tool for Digital Forensics and Incident Response (DFIR). It allows investigators to collect and process forensically useful artifacts within minutes.

This documentation serves as a complete, searchable index of all currently available **Targets** and **Modules** within the KAPE ecosystem.

### **Understanding the Ecosystem**

{% tabs %}

{% tab title="🎯 Targets (.tkape)" %}

**Targets** are essentially roadmaps for KAPE. They tell KAPE exactly *what* files and directories to copy from a suspect system.

If you need to collect the $MFT, Windows Event Logs, or Chrome browsing history, you use a Target.

{% endtab %}

{% tab title="⚙️ Modules (.mkape)" %}

**Modules** run programs against the data you just collected. They tell KAPE exactly *how* to process the evidence.

If you want to parse that $MFT into a readable CSV using MFTECmd, or scan collected files with Thor, you use a Module.

{% endtab %}

{% endtabs %}

## **How to use this GitBook**

We have organized the KAPE repository into **Investigative Categories** via the sidebar on the left.

Whether you are looking for evidence of lateral movement via Remote Access tools, or trying to parse volatile memory dumps, select the relevant category on the left to see all associated Targets and Modules.

{% hint style="info" %}

**Pro-Tip:** Use the search bar (Cmd+K or Ctrl+K) anywhere in this documentation to instantly find a specific tool, author, or artifact\!

{% endhint %}