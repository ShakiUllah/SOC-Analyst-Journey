# Learning Write-up: TryHackMe - Windows Forensics 1

> This document provides a detailed summary of the concepts and techniques covered in the "Windows Forensics 1" room on TryHackMe, completed on September 15, 2025. This was a deep-dive into host-based forensics, focusing on the Windows Registry as a primary source of evidence for post-mortem incident response investigations.

---

## Key Concepts & Techniques Covered

The room provided a comprehensive workflow for a forensic investigation, progressing from foundational theory and evidence acquisition to the detailed analysis of specific digital artifacts.

### 🏛️ The Windows Registry as Forensic Evidence
The investigation centered on the **Windows Registry**, a hierarchical database that stores critical configuration settings and historical data for the operating system and installed applications. For a forensic analyst, the registry is a goldmine of information. It provides a timeline of events, revealing user actions, program executions, and changes to the system configuration long after they have occurred. Understanding its structure is fundamental to any Windows-based investigation.

### 💾 Data Acquisition & Offline Analysis
A core principle of digital forensics is the preservation of evidence. To prevent alteration of the live system, the room covered the process of **Data Acquisition**. This involves extracting the raw registry hive files (e.g., from `C:\Windows\System32\config`) from a disk image or a non-running system. This allows for **Offline Analysis**, where an investigator can safely examine the registry data in a controlled forensic environment without contaminating the original evidence.

### 🕵️ Investigating User & System Activity
The core of the room was a detailed exploration of specific registry hives to uncover different types of forensic evidence. This hands-on analysis is critical for piecing together the story of what happened on a compromised machine.

- **System Information and Accounts:** The initial steps of any investigation involve understanding the system itself. By analyzing the **SYSTEM** and **SAM** hives, I was able to extract key information such as the exact operating system version, the original installation date, the computer's hostname, and a list of local user accounts.

- **Usage of Files/Folders (User Activity):** To understand what a specific user was doing, I analyzed their personal **NTUSER.DAT** hive. This file contains a wealth of information, including **Most Recently Used (MRU)** lists and **Shellbags**, which reveal the specific files, folders, and applications the user has recently accessed, providing a clear picture of their activity.

- **Evidence of Execution:** A key task in malware analysis is proving that a malicious program was actually run. I investigated specific registry keys like **UserAssist** (which tracks the execution of GUI-based programs) and **ShimCache** (which logs application compatibility information) to find definitive, timestamped evidence of program execution, even for programs that have been deleted.

- **External Device/USB Forensics:** To investigate potential data theft or the introduction of malware from an external source, I analyzed the `SYSTEM\ControlSet001\Enum\USBSTOR` key. This registry location provided a detailed history of all USB storage devices that had been connected to the machine, including vendor and product IDs, unique serial numbers, and crucial timestamps of their first and last use.

### 🏆 Hands-on Challenge
The room culminated in a final hands-on challenge. I was provided with a set of acquired registry hives from a simulated case and was required to use the techniques learned to conduct a full investigation. This involved extracting specific pieces of evidence to answer questions about the user's actions, the programs they ran, and any external devices they connected, solidifying the practical application of the concepts.

*Evidence of Completed Challenge:*
- [!](../Screenshots/Day9_WIN4N6.png)
- [!](../Screenshots/Day9_WIN4N62.png)
- [!](../Screenshots/Day9_WIN4N63.png)

---

## 🎓 Key Skills Learned
- **In-depth Windows Registry Analysis:** Detailed examination of key hives (`SYSTEM`, `SAM`, `SOFTWARE`, `NTUSER.DAT`) and their forensic significance.
- **Digital Forensics & Incident Response (DFIR):** Application of a methodical forensic process, from evidence acquisition to detailed analysis and reporting.
- **Offline Hive Analysis:** The critical skill of working with extracted registry files to preserve evidence integrity.
- **Evidence of Execution Tracking:** Using forensic artifacts like UserAssist and ShimCache to prove program execution.
- **USB Device Investigation:** The ability to find and interpret evidence of connected external storage devices.
