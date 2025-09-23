# Cybersecurity Labs  

A collection of my hands-on cybersecurity projects, built in my home lab to practice **SOC analyst workflows, detection engineering, and incident response**.  

I use this repo to document my learning process, share configurations, and showcase detection techniques aligned with the **MITRE ATT&CK framework**.  

---

## 🔹 Lab Overview  

- **SIEM:** Wazuh (log collection, alerting, correlation)  
- **IDS:** Suricata (network intrusion detection, custom rule writing)  
- **Endpoints:** Windows 11 VM (with Sysmon), Ubuntu/Kali Linux  
- **Networking Tools:** Nmap, Wireshark  
- **Scripting:** PowerShell, Bash  

---

## 🔹 Projects  

### 1. Home SOC Lab: Wazuh SIEM  
- Deployed Wazuh for centralized log collection.  
- Integrated Windows (Sysmon) and Linux endpoints.  
- Built detection rules mapped to MITRE ATT&CK (brute force, privilege escalation, persistence).  
- **Skills:** SIEM, Log Analysis, Incident Response.  

📸 *Example Alert Screenshot:*  
![Wazuh Alerts](images/wazuh-alerts.png)  

---

### 2. Suricata IDS & Custom Rule Writing  
- Deployed Suricata to monitor network traffic.  
- Wrote custom rules to detect:  
  - Brute force attempts  
  - Port scanning  
  - Suspicious PowerShell activity  
- Tuned alerts to reduce false positives.  
- **Skills:** IDS/IPS, Detection Engineering, Network Security.   

---

### 3. Windows Event Logging with Sysmon  
- Configured Sysmon for advanced event collection.  
- Forwarded logs to Wazuh for correlation.  
- Detected simulated persistence and lateral movement.  
- **Skills:** Sysmon, Windows Event Logging, Threat Detection.  

---

### 4. Threat Detection Playbook  
- Documented detection and response workflows for:  
  - Brute force login attempts  
  - Malware execution  
  - Privilege escalation  
- Created repeatable incident response steps.  
- **Skills:** Threat Hunting, MITRE ATT&CK, Incident Response.  

---

### 5. Network Scanning & Reconnaissance  
- Conducted scans with Nmap to discover open ports & services.  
- Simulated attacker reconnaissance.  
- Compared results with vulnerability scans.  
- **Skills:** Nmap, Recon, Vulnerability Testing.  

---

## 🔹 How to Use This Repo  

- Each folder contains documentation, configs, and screenshots for a lab.  
- Files are organized so others can reproduce the labs in their own environment.  
- Example workflow:  
  1. Review project README.  
  2. Deploy VM(s).  
  3. Import configuration files.  
  4. Recreate detection & analyze alerts.  

---

## 🔹 Roadmap  

- Add more MITRE ATT&CK technique coverage  
- Expand Suricata rules (HTTP, DNS, C2 detection)  
- Integrate Elastic Stack dashboards  
- Document incident response “case studies”  

---

## 🔹 Author  

**Dominic “DJ” Jones**  
- Aspiring Tier 1 SOC Analyst (San Antonio, TX)  
- Currently working toward **CompTIA A+ & Security+**  
- Building hands-on skills in detection engineering & incident response  

🔗 [Connect with me on LinkedIn](https://linkedin.com/in/)  
🔗 [More projects coming soon]  
