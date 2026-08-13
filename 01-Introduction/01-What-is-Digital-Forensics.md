# Digital Forensics

## 1. What is Digital Forensics?

**Digital Forensics** is the process of identifying, collecting, preserving, examining, analyzing, and documenting digital evidence to determine what happened during a security incident.

It is used to answer questions such as:

- What happened?
- When did it happen?
- How did the attack happen?
- Which user or system was involved?
- What files or data were affected?
- What actions did the attacker perform?
- Did the attacker establish persistence?
- What evidence supports the findings?

---

## 2. Why is Digital Forensics Important?

Digital forensics helps security teams investigate:

- Malware infections
- Phishing attacks
- Ransomware incidents
- Account compromise
- Unauthorized access
- Data theft
- Insider threats
- Suspicious processes
- Privilege escalation
- Persistence
- Lateral movement
- Command and Control (C2) activity

It helps investigators reconstruct the attack and determine the **root cause, timeline, and impact**.

---

## 3. Main Objectives

The main objectives of digital forensics are:

1. Identify relevant evidence.
2. Preserve evidence integrity.
3. Collect evidence safely.
4. Examine digital artifacts.
5. Analyze evidence.
6. Reconstruct the incident timeline.
7. Identify attacker activity.
8. Identify Indicators of Compromise (IOCs).
9. Determine the root cause.
10. Determine the impact.
11. Document findings.
12. Produce an investigation report.

---

## 4. Digital Forensics in a SOC

Digital forensics is mainly used when a SOC alert requires deeper investigation.

### Example

```text
SIEM / EDR Alert
       ↓
Suspicious Activity
       ↓
SOC Analyst Triage
       ↓
Evidence Collection
       ↓
Forensic Analysis
       ↓
Timeline Reconstruction
       ↓
IOC / TTP Identification
       ↓
Root Cause Analysis
       ↓
Incident Response
