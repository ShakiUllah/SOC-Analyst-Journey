# 🛡️ SOC Analyst Journey

Welcome to my **SOC Analyst Journey Repository** 🚀  
This repo documents my **30-day free SOC Analyst roadmap**, where I practice real-world SOC/Blue Team tasks, build case studies, and share my progress.

---

## 📂 Repository Structure

```
SOC-Analyst-Journey/
│
├── README.md
├── Case_Studies/        # Daily/weekly case studies
├── Screenshots/         # Screenshots supporting case studies
├── Detection_Rules/     # Custom Wazuh/Suricata/Snort rules
├── Queries/             # Detection queries (Splunk, Kibana, Wazuh)
└── Portfolio/           # Final SOC portfolio + reports
```

---

## 📅 Case Studies

### ✅ Week 1 – Log Analysis Basics
- [Day 1: Failed SSH Login Attempts](Case_Studies/Day1_Failed_SSH_Logins.md)  
- [Day 2: Successful vs Failed Logins (Linux)](Case_Studies/Day2_Successful_vs_Failed_Logins.md)  
- [Day 3: Syslog Analysis](Case_Studies/Day3_Syslog_Analysis.md)  
- Day 4: Windows Process Creation Logs (adapted on Linux)  
- Day 5: TryHackMe Linux Fundamentals 1  
- Day 6: TryHackMe Windows Fundamentals 1  
- Day 7: **Case Study 1 Summary Report**

### 🔎 Week 2 – SIEM & Log Monitoring
- Day 8: Install Wazuh SIEM  
- Day 9: Ingest Linux Logs into Wazuh  
- Day 10: Detect Brute-Force in Wazuh  
- Day 11: Custom Wazuh Rule (Multiple Failed Logins)  
- Day 12: TryHackMe Intro to Log Analysis  
- Day 13: Apache Log Analysis  
- Day 14: **Case Study 2 Summary Report**

### 🛡️ Week 3 – IDS/IPS & Threat Hunting
- Day 15: Install Suricata IDS  
- Day 16: Detect Nmap Scan with Suricata  
- Day 17: Write Suricata Detection Rules  
- Day 18: Wireshark HTTP PCAP Analysis  
- Day 19: TryHackMe Snort Challenge  
- Day 20: TryHackMe Wireshark 101  
- Day 21: **Case Study 3 Summary Report**

### 🚨 Week 4 – Incident Response & Portfolio
- Day 22: SOC Workflow (Alert → Triage → Escalation)  
- Day 23: Mock Incident (SSH Brute Force Report)  
- Day 24: Phishing Investigation (LetsDefend)  
- Day 25: TryHackMe Blue Team Fundamentals  
- Day 26: Document Detection Queries (Splunk/Wazuh)  
- Day 27: **Case Study 4 Summary Report**  
- Day 28–30: Final SOC Portfolio & LinkedIn Showcase  

---

## 📷 Screenshots
Supporting screenshots for each case study are stored in the [Screenshots/](Screenshots) folder.  

Example:  
- `Day1_ssh_attempt.png` → Wrong login attempt  
- `Day1_log_output.png` → Auth.log showing failed attempts  

---

## ⚙️ Detection Rules
Custom rules for Wazuh, Suricata, or Snort will be stored in the [Detection_Rules/](Detection_Rules) folder.  

Example:  
- `wazuh_failed_login_rule.xml`  
- `suricata_bruteforce.rules`  

---

## 🔎 Detection Queries
Queries for SIEM tools (Splunk, Kibana, Wazuh) will be stored in the [Queries/](Queries) folder.  

Example:  
- `splunk_bruteforce_query.spl`  
- `wazuh_failed_login_query.txt`  

---

## 📑 Portfolio
The final **SOC Analyst Portfolio** will be stored in the [Portfolio/](Portfolio) folder, including:  
- SOC Portfolio Report (PDF)  
- Final Case Study Reports (Markdown)  
- Incident Response Reports  

---

## 📌 About This Project
- 🖥️ Focus: SOC Analyst (Blue Team) skills  
- 🆓 All tools and labs are free (Wazuh, Suricata, Wireshark, TryHackMe free rooms, LetsDefend, Forage internships, Microsoft Learn, Cisco Cybersecurity Essentials).  
- 📈 Goal: Build a **public portfolio** to demonstrate real SOC skills for entry-level cybersecurity roles.  

---

## 📢 Connect with Me
- LinkedIn: [Your LinkedIn Profile](https://www.linkedin.com/in/shakir-ullah-161273377/) 
- GitHub: [Your GitHub Profile](https://github.com/your-username)  

---
