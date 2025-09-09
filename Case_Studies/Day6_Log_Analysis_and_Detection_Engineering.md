# Learning Write-up: TryHackMe - Log Analysis & Detection Engineering

> This document summarizes the key concepts and tools covered in the comprehensive 'Intro to Log Analysis' room on TryHackMe, completed on September 9, 2025.

---

[Completed Room](../screenshots/Day6_completed_room.png)

---

## Key Topics Covered

The room provided a holistic overview of a security analyst's workflow, from foundational theory to advanced detection engineering concepts. The key areas are detailed below.

### 🏛️ Foundational Theory
A strong investigation starts with a solid theoretical base. This section covered:
- **Log Analysis Basics:** The core principles of what logs are and why they are the primary source of evidence in any digital investigation.
- **Investigation Theory:** A methodical approach to analyzing events, forming hypotheses, and pivoting between data points to uncover the full story of an incident.
- **Automated vs. Manual Analysis:** Understanding the trade-offs between using a SIEM for automated correlation and the necessity of manual, command-line analysis for deep-dive investigations.

---

### 🛠️ Practical Tools of the Trade
This section focused on the hands-on tools that an analyst uses daily to parse and understand log data.
- **Command Line Tools:** Mastery of essential commands like `grep` for searching and filtering through massive text-based log files.
- **Regular Expressions (RegEx):** The ability to create powerful and precise search patterns to find specific, needle-in-a-haystack log entries.
- **CyberChef:** Hands-on practice with the "Cyber Swiss Army Knife" for decoding, deobfuscating, and transforming data from logs into a human-readable format.

*Below is an example of a tool used during the practical exercises:*
- ![Command Line Log Analysis](../screenshots/Day6_command_line_log_analysis.png)
- ![CyberChef Example](../screenshots/Day6_cyberchef_analysis.png)

---

### 🔬 Introduction to Detection Engineering
The most advanced section covered the proactive side of defense: building the detections themselves.
- **Detection Engineering:** The process of identifying threat behaviors and creating rules and alerts to catch them automatically in the future.
- **Yara:** An introduction to using Yara rules to identify and classify malware based on textual or binary patterns.
- **Sigma:** A deep dive into Sigma, the generic signature format for SIEM systems. This is a critical skill, as it allows defenders to write one detection rule that can be translated to work on any platform (Wazuh, Splunk, QRadar, etc.).

*Below is an example of a detection rule discussed in the room:*
- ![Sigma Rule Example](../screenshots/Day6_sigma_rule.png)
- ![Yara Rule Example](../screenshots/Day6_yara_rule.png)
---

## My Key Takeaways

- The power of **Sigma** rules to create vendor-agnostic detections is a game-changer for a SOC. I can now understand how to read these rules and apply them to my own Wazuh lab.
- Learning to use **CyberChef** is essential. It can save hours of manual work when dealing with encoded or obfuscated commands found in malicious scripts.
- A good analyst needs to be skilled in both **automated analysis** (in a SIEM like Wazuh) and **manual analysis** (on the command line). One is for speed, the other is for depth.
