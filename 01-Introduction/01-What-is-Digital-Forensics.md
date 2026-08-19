# 🔎 Digital Forensics – Fundamentals

## 1. What is Digital Forensics?

Digital Forensics is the process of **identifying, collecting, preserving, examining, analyzing, and presenting digital evidence** from computers, mobile devices, networks, storage devices, and other digital systems.

The main goal is to determine:

- What happened?
- When did it happen?
- How did it happen?
- Which files or systems were affected?
- Who or what was responsible?
- What evidence supports the findings?

### Simple Example

Suppose an employee's computer is suspected of being compromised.

A forensic investigator may analyze:

- Login activity
- Downloaded files
- Browser history
- USB devices
- Deleted files
- Windows Event Logs
- Running processes
- File metadata
- Network activity

The investigator then uses this evidence to reconstruct what happened.

---

# 2. Objectives of Digital Forensics

The major objectives are:

1. Identify digital evidence
2. Preserve evidence without modification
3. Recover useful information
4. Analyze system activity
5. Determine the timeline of events
6. Identify Indicators of Compromise (IOCs)
7. Determine the root cause of an incident
8. Document findings
9. Present evidence in a clear and defensible manner

---

# 💾 3. Digital Evidence

## What is Digital Evidence?

Digital evidence is any information stored or transmitted in digital form that can help prove or explain an event.

### Examples

- Files
- Emails
- Browser history
- Chat messages
- Images
- Videos
- Documents
- Windows Event Logs
- System logs
- Registry artifacts
- Network captures
- Metadata
- Deleted files
- USB device information
- Application logs

---

# 4. Types of Digital Evidence

Digital evidence can come from many sources.

### 4.1 Computer Evidence

Examples:

- Hard disks
- SSDs
- RAM
- Operating system files
- User files
- Logs

### 4.2 Network Evidence

Examples:

- PCAP files
- Firewall logs
- IDS/IPS logs
- DNS logs
- Proxy logs
- NetFlow data

### 4.3 Mobile Evidence

Examples:

- Call logs
- SMS
- Application data
- GPS information
- Photos
- Browser history

### 4.4 Cloud Evidence

Examples:

- Cloud audit logs
- Authentication logs
- Cloud storage files
- API activity
- IAM activity

---

# 5. Digital Forensics Process

A typical forensic investigation follows these stages:

```text
Identification
      ↓
Collection
      ↓
Preservation
      ↓
Examination
      ↓
Analysis
      ↓
Documentation
      ↓
Reporting
```
# 6. Identification

Identification is the process of determining:

- What happened?
- Which systems are involved?
- What evidence may exist?
- Where is the evidence located?
- 
Example:

A company detects suspicious activity on a Windows workstation.

Potential evidence sources:

- Hard disk
- Windows Event Logs
- Browser history
- Registry
- Prefetch
- User files
- USB history

#  7. Collection

Collection involves acquiring relevant digital evidence.

Examples:

- Creating a forensic image of a hard disk
- Collecting log files
- Capturing RAM
- Exporting browser artifacts
- Collecting network captures

The investigator must ensure that evidence is collected in a controlled manner.

#  8. Preservation

Preservation means protecting evidence from:

- Modification
- Deletion
- Corruption
- Contamination

The original evidence should be preserved whenever possible.

Investigators generally work on a forensic copy/image instead of directly modifying the original evidence.

#  9. Forensic Image

A forensic image is a bit-by-bit copy of a storage device or partition.

It attempts to preserve the contents of the original storage media, including:

- Active files
- Deleted files
- File system structures
- Unallocated space
- Metadata

### Common Forensic Image Formats
| Format | Description |
| ------ | ----------- |
| E01    | EnCase Expert Witness format |
| AFF    | Advanced Forensic Format |
| RAW/DD | Raw bit-by-bit disk image |

## E01

E01 is one of the commonly encountered forensic image formats.

Autopsy can analyze E01 images.

Example:
```text
2020JimmyWilson (1).E01
```
This is the type of forensic image we will analyze in the Autopsy project.

---

# 10. Hashing

Hashing is used to generate a unique-looking value from digital data.

Common hashing algorithms include:

- MD5
- SHA-1
- SHA-256

Example:
```text
File
 ↓
Hash Algorithm
 ↓
SHA-256 Hash
```
If the file changes, its hash value will normally change.

### Why is Hashing Important?

Hashing can help verify:

- Evidence integrity
- File integrity
- Whether a forensic image has changed
- Whether two files are identical
Example:
```text
Original Evidence
      ↓
Calculate Hash
      ↓
Create Forensic Image
      ↓
Calculate Hash Again
      ↓
Compare Hashes
```
If the expected hash values match, this provides evidence that the data remained unchanged.

---

#  11. Chain of Custody

Chain of Custody is the documented history of evidence from the moment it is collected until the investigation is completed.

It records:

- Who collected the evidence
- When it was collected
- Where it was collected
- Who handled it
- Why it was transferred
- Where it was stored
- What actions were performed

Example:
```text
Evidence Identified
       ↓
Collected by Investigator A
       ↓
Stored securely
       ↓
Transferred to Investigator B
       ↓
Analyzed
       ↓
Reported
```

A proper chain of custody helps demonstrate that evidence was handled properly.

---

# 12. Metadata

Metadata is information that describes another piece of data.

For a file, metadata may include:

- File name
- File size
- File type
- Creation time
- Modified time
- Access time
- File permissions
- Author
- Location information
- Application used to create the file

Example:
```text
File: suspicious.docx

Created: 2026-08-10 10:15
Modified: 2026-08-10 10:20
Author: John
Type: Microsoft Word Document
```
Metadata can provide useful investigative clues.

---

# 13. File System

A file system controls how files are stored and organized on a storage device.

Common file systems include:

- NTFS
- FAT32
- exFAT
- ext3
- ext4
- APFS

## NTFS

NTFS is commonly used by modern Windows systems.

Important NTFS forensic artifacts include:

- $MFT
- $LogFile
- $UsnJrnl
- $Bitmap

These artifacts can provide information about file activity.

---

# 14. Deleted Files

Deleting a file does not always mean that its data immediately disappears from the storage device.

Depending on the file system and storage technology, forensic tools may be able to recover information from:

- File system metadata
- Unallocated space
- File system remnants
- Recycle Bin
- Application artifacts

### Important Concept
```text
User deletes file
       ↓
File may become logically deleted
       ↓
File system marks space as available
       ↓
Data may remain until overwritten
```
Forensic tools can sometimes recover such information.

---

# 15. Windows Artifacts

Windows systems contain many artifacts useful for forensic investigations.

Important examples include:

| Artifact         | What it can help reveal |
| ---------------- | ----------------------- |
| Windows Event Logs | System and security activity |
| Registry           | System and user configuration |
| Prefetch           | Application execution evidence |
| Amcache            | Application execution information |
| Shimcache          | Program execution-related information |
| UserAssist         | GUI application activity |
| Recycle Bin        | Deleted files |
| Browser History    | Web activity |
| LNK Files          | File/application access information |
| Jump Lists         | Recently accessed files/applications |
| `$MFT`             | File system metadata |

---

# 16. Windows Event Logs

Windows Event Logs are extremely important in SOC and digital forensics.

Common logs include:

- Security
- System
- Application
- PowerShell
- Windows Defender

Important Security Event IDs

### Important Security Event IDs

| Event ID | Description |
| -------- | ----------- |
| 4624     | Successful logon |
| 4625     | Failed logon |
| 4688     | Process creation |
| 4720     | User account created |
| 4728     | Member added to a global security-enabled group |
| 4732     | Member added to a local security-enabled group |

These events can help reconstruct attacker activity.

--- 

# 17. Browser Forensics

Browser artifacts can provide information about a user's web activity.

Potential evidence includes:

- Browsing history
- Downloads
- Cookies
- Cached files
- Bookmarks
- Search history
- Saved sessions

Supported browsers may include:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox

---

# 18. Timeline Analysis

Timeline analysis organizes events according to time.

Example:
```text
09:10 → User logged in
09:12 → Browser opened
09:15 → File downloaded
09:17 → PowerShell executed
09:20 → Suspicious file created
09:22 → External connection observed
```
This helps investigators understand the sequence of events.

---

# 19. Indicators of Compromise (IOCs)

An IOC is an artifact that may indicate malicious activity or compromise.

Examples:

- Malicious IP address
- Malicious domain
- Suspicious URL
- File hash
- Suspicious filename
- Malicious process
- Registry modification
- Suspicious PowerShell command
Example:
```
IOC:
File Hash = abc123...

Type:
SHA-256

Finding:
Hash matches a known malicious file
```

---

# 20. Digital Forensics vs Incident Response

These concepts are related but different.

Incident Response

Focuses on:

Detect
- Respond
- Contain
- Eradicate
- Recover
## Digital Forensics

Focuses on:

Collect
- Preserve
- Examine
- Analyze
- Report

---

# 21. Digital Forensics Tools

Common tools include:

### Autopsy

Used for digital forensic investigation and analysis of disk images.

### FTK

Forensic investigation and evidence analysis platform.

### EnCase

Digital forensic investigation platform.

### Volatility

Used primarily for memory/RAM forensic analysis.

### Wireshark

Used for network traffic analysis.

### Eric Zimmerman Tools

A collection of Windows forensic analysis tools.


#  22. Autopsy

Autopsy is an open-source digital forensics platform.

It provides a graphical interface for analyzing forensic evidence.

Autopsy can help investigators examine:

- Disk images
- Files
- Deleted files
- File metadata
- Browser activity
- Windows artifacts
- Hashes
- Keywords
- Timeline information
- User activity

### Basic Autopsy Workflow
```text
Create Case
     ↓
Add Data Source
     ↓
Select E01 / Disk Image
     ↓
Configure Ingest Modules
     ↓
Run Analysis
     ↓
Review Artifacts
     ↓
Investigate Findings
     ↓
Create Report
```
---

# 23. Example Forensic Investigation

Suppose a suspicious document was downloaded on a Windows computer.

The investigator could follow this process:
```text
1. Acquire forensic image
        ↓
2. Verify evidence integrity
        ↓
3. Load image into Autopsy
        ↓
4. Analyze file system
        ↓
5. Search for suspicious document
        ↓
6. Examine metadata
        ↓
7. Check browser download history
        ↓
8. Check Windows Event Logs
        ↓
9. Check process execution artifacts
        ↓
10. Identify IOCs
        ↓
11. Build timeline
        ↓
12. Document findings
```
---

# 24. Key Terms to Remember

| Term | Meaning |
| ---- | ------- |
| Digital Evidence | Information that can support an investigation |
| Forensic Image | Bit-by-bit copy of storage media |
| E01 | Common forensic image format |
| Hash | Value used to help verify data integrity |
| Chain of Custody | Record of evidence handling |
| Metadata | Data describing another piece of data |
| Artifact | Evidence left behind by system/user activity |
| IOC | Indicator that may suggest compromise |
| Timeline | Chronological representation of events |
| Unallocated Space | Storage space not currently assigned to active files |
| File System | Structure used to organize and manage files |
| Autopsy | Digital forensics analysis platform |
