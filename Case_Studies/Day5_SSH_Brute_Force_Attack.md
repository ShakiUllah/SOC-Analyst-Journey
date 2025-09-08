# Case Study: Detection of a Simulated SSH Brute-Force Attack

## Summary

On September 8, 2025, a simulated SSH brute-force attack was launched against a host monitored by a Wazuh SIEM. The SIEM successfully detected the activity, generating critical alerts for both the initial brute-force attempt (Rule ID 5712) and the subsequent successful login (Rule ID 5716), indicating a full compromise of the user account.

## Tools Used

* **Wazuh SIEM:** For security monitoring, log analysis, and alerting.
* **Hydra:** For simulating the brute-force attack.
* **OpenSSH Server:** The target service.

## Analysis and Timeline

The exercise was conducted to test the detection capabilities of the Wazuh SIEM against a common threat vector.

**1. Attack Simulation:**
[cite_start]At approximately 16:05 PM PKT on September 8, 2025, a brute-force attack was initiated using Hydra against the user 'shakir' on the local machine. The attack utilized a small, custom password list.

* **Evidence of Attack:**
    ## 📷 Screenshot
- ![Attack Simulation](../Screenshots/Day5_Attack Simulation)

**2. Initial Brute-Force Detection:**
Immediately following the attack, Wazuh began correlating the multiple failed login attempts. This triggered a Level 10 alert **(Rule ID: 5712)** for an "SSHD brute-force attack," indicating a potential security risk.

* **Evidence of Initial Detection:**
 ## 📷 Screenshot
- ![Brute-Force Detection](../Screenshots/Day5_WAZUH_ALERT)

**3. Critical Alert - Successful Compromise:**
[cite_start]At 16:17 PM PKT, Wazuh escalated the event by triggering a Level 12 alert **(Rule ID: 5716)** for "Multiple authentication failures followed by a success." This critical alert confirmed that the simulated attacker's attempts were not only detected but had resulted in a successful login, representing a compromised account.

* **Evidence of Compromise:**
    ## 📷 Screenshot 
- ![Successful Compromise](../Screenshots/Day5_WAZUH_ALERT2)

## Indicators of Compromise (IoCs)

The following forensic evidence was collected from the alerts:

* **Attacker IP Address:** `127.0.0.1`
* **Target Username:** `shakir`
* **Target Service:** SSH (Port 22)
* **Key Wazuh Rule IDs:** `5712`, `5716`

## Conclusion

The Wazuh SIEM performed effectively, successfully detecting and alerting on a simulated SSH brute-force attack. The correlation of multiple failed logins into a single brute-force alert, and the further escalation upon a successful login, demonstrates a mature detection capability for this common threat vector. This exercise validates the lab environment's ability to identify and escalate credential-based attacks in near real-time.
