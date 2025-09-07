# 🚀 Day 4 – Wazuh Local Agent Lab (SOC Analyst Journey)

Today I explored how **Wazuh works locally** on my own Ubuntu machine without installing a separate agent.  
The Wazuh Manager comes with a **built-in local agent (ID: 000)** that can monitor system activity, logs, file changes, and even USB device connections.  

---

## 🔹 Step 1: Check Wazuh Manager Status
Make sure the manager is running:

```bash
sudo systemctl status wazuh-manager
```

If it’s stopped:

```bash
sudo systemctl start wazuh-manager
sudo systemctl enable wazuh-manager
```

---

## 🔹 Step 2: Verify Local Agent
List active agents (notice `000` is the local agent):

```bash
sudo /var/ossec/bin/agent_control -l
```

📸 (../Screenshots/Day4_Local_Agent.png)  

---

## 🔹 Step 3: Trigger Alerts Locally

### ✅ a) File Monitoring
Create and edit a test file:
```bash
sudo touch /etc/test_wazuh_file
sudo echo "Wazuh test alert" >> /etc/test_wazuh_file
```

---

### ✅ b) Sudo Command Usage
Wazuh monitors `sudo` activity:
```bash
sudo ls /root
sudo cat /var/log/auth.log
```

---

### ✅ c) USB Device Detection
Plug in a USB and check kernel logs:
```bash
dmesg | tail
```

---

### ✅ d) Log Activity
Add text into syslog:
```bash
sudo echo "Testing log alert" >> /var/log/syslog
```

---

## 🔹 Step 4: Monitor Alerts in Real-Time
Alerts are stored in JSON format:

```bash
sudo tail -f /var/ossec/logs/alerts/alerts.json
```

📸 (../Screenshots/Day4_json_file.png)  

---

## 🔹 Step 5: Check Wazuh Internal Logs
View internal manager + agent activity:
```bash
sudo tail -f /var/ossec/logs/ossec.log
```

---

## ✅ Summary
- Wazuh Manager has a **built-in local agent (000)**.  
- I triggered events with:
  - File changes  
  - Sudo commands  
  - USB connection  
  - Log activity  
- I monitored alerts in:
  - `alerts.json` → actual security alerts  
  - `ossec.log` → internal manager/agent logs  
- This helped me understand how Wazuh monitors activity **without deploying extra agents**.  

Next step 👉 I will install a **VM** and deploy Wazuh agents on other machines to simulate a real SOC environment.  
