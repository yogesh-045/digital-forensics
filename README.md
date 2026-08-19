# 🔎 Digital Forensics

A structured collection of **Digital Forensics concepts, tools, techniques, artifacts, and practical investigations** for cybersecurity and SOC/DFIR learning.

---

## 📌 What's Inside?

This repository covers the following areas:

### 🧠 Digital Forensics Fundamentals
- Digital Evidence
- Evidence Acquisition
- Evidence Preservation
- Forensic Imaging
- E01 / RAW Image Formats
- Hashing & Evidence Integrity
- Chain of Custody
- Forensic Investigation Process

### 💽 File System Forensics
- NTFS
- MFT (`$MFT`)
- `$LogFile`
- `$UsnJrnl`
- `$Bitmap`
- File Metadata
- MACB Timestamps
- Deleted Files
- Unallocated Space
- File Carving
- Alternate Data Streams (ADS)

### 🪟 Windows Forensics
- Windows Registry
- Registry Hives
- NTUSER.DAT
- SYSTEM
- SOFTWARE
- SAM
- SECURITY
- Prefetch
- Amcache
- Shimcache
- UserAssist
- LNK Files
- Jump Lists
- Recycle Bin
- SRUM
- Windows Event Logs
- PowerShell Artifacts

### 🌐 Browser & User Activity Forensics
- Browser History
- Downloads
- Cookies
- Cache
- Bookmarks
- Search Activity
- User Activity
- USB Device Artifacts
- Recent Files

### 🕐 Timeline & Artifact Analysis
- Timeline Reconstruction
- Timestamp Analysis
- Artifact Correlation
- Event Correlation
- User Activity Reconstruction
- IOC Identification

### 🧠 Memory Forensics
- RAM Analysis
- Process Analysis
- Network Connections
- DLL Analysis
- Command-Line Analysis
- Memory-Based Malware Detection
- Volatility

### 🦠 Malware & Attack Forensics
- Malware Execution
- Persistence
- Process Analysis
- Registry Modifications
- Suspicious PowerShell Activity
- C2 Activity
- Data Collection
- Exfiltration Evidence

### 🚨 IOC & Threat Analysis
- File Hashes
- IP Addresses
- Domains
- URLs
- Suspicious Files
- Processes
- Registry Indicators
- IOC Correlation
- MITRE ATT&CK Mapping

---

## 🛠️ Tools

Tools covered in this repository include:

- 🔬 **Autopsy**
- 🧠 **Volatility**
- 🛠️ **FTK**
- 🔎 **EnCase**
- 🧰 **KAPE**
- 🪟 **Eric Zimmerman Tools**
- 📊 **Plaso**
- 🔍 **RegRipper**
- 🌐 **Wireshark**
- 🧪 **CyberChef**

---

## 🧪 Practical Investigations

This repository also contains hands-on forensic investigations and case-based analysis.

### 📁 Current Case Study

**2020 Jimmy Wilson Forensic Investigation**

Evidence:

```text
2020JimmyWilson (1).E01
```
The investigation includes:

- Evidence examination
- File system analysis
- Metadata analysis
- Keyword investigation
- Deleted file analysis
- Browser artifact analysis
- Windows artifact analysis
- Timeline analysis
- IOC identification
- Evidence correlation
- Investigation findings

```text
📂 Repository Structure
Digital-Forensics/
│
├── README.md
│
├── 01-Fundamentals/
│   └── Digital-Forensics-Basics.md
│
├── 02-File-System-Forensics/
│   ├── NTFS.md
│   ├── MFT.md
│   └── File-Carving.md
│
├── 03-Windows-Forensics/
│   ├── Windows-Registry.md
│   ├── Windows-Event-Logs.md
│   └── Windows-Artifacts.md
│
├── 04-Browser-Forensics/
│   └── Browser-Artifacts.md
│
├── 05-Memory-Forensics/
│   └── Volatility.md
│
├── 06-Timeline-Analysis/
│   └── Timeline-Analysis.md
│
├── 07-IOC-Analysis/
│   └── IOC-Correlation.md
│
├── 08-Autopsy/
│   └── Autopsy-Notes.md
│
└── 09-Practical-Cases/
    └── Jimmy-Wilson/
        ├── Case-Overview.md
        ├── Findings.md
        └── Evidence-Analysis.md
  ```
# 🎯 Learning Objectives

By working through this repository, the goal is to develop practical understanding of:

- 🔍 Digital evidence analysis
- 💽 Forensic image investigation
- 🪟 Windows artifact analysis
- 🗂️ File system forensics
- 🕐 Timeline reconstruction
- 🚨 IOC identification
- 🧠 Memory forensics
- 🛠️ Forensic investigation tools
- 🎯 MITRE ATT&CK mapping
- 📝 Forensic reporting

## 🚀 Status

Learning & Practical Investigation — In Progress
