# 🔐 Cyber Security Internship - Task 4

## Report: Setup and Use a Firewall on Windows/Linux  

**Name:** Dishanyaa Shrii K M  
**Date & Time:** 29-09-2025, 09:45 AM (IST)  
**Task 4:** Setup and Use a Firewall on Windows/Linux  

---

## 📌 Objective  
Configure and test basic firewall rules to allow or block traffic using either **Windows Firewall** or **UFW (Uncomplicated Firewall)** on Linux.  

---

## 🛠 Tools Used  
- Linux Firewall (**UFW**)  
- **nc (netcat)** for testing  
- Command-line interface (**Kali Linux**)  

---

## 📖 Key Concepts  
- **Firewall Configuration** → Defining rules to allow or deny network traffic.  
- **Traffic Filtering** → Blocking insecure services (Telnet on port 23) while allowing secure ones (SSH on port 22).  
- **Ports** → Logical endpoints used for communication (e.g., 22 = SSH, 23 = Telnet).  
- **UFW** → A simple interface for managing `iptables` in Linux.  

---

## ⚡ Steps Performed  

1. **Installed UFW (if not present):**  
   ```bash
   sudo apt update && sudo apt install ufw -y
   ```  

2. **Enabled UFW:**  
   ```bash
   sudo ufw enable
   ```  

3. **Allowed SSH (Port 22):**  
   ```bash
   sudo ufw allow 22/tcp
   ```  

4. **Listed current firewall rules:**  
   ```bash
   sudo ufw status numbered
   ```  

5. **Blocked Telnet (Port 23):**  
   ```bash
   sudo ufw deny 23/tcp
   ```  

6. **Tested blocked port using Netcat:**  
   ```bash
   nc -zv 127.0.0.1 23
   ```  
   ✅ *Result: Connection refused/blocked.*  

7. **Removed the test rule (restore original state):**  
   ```bash
   sudo ufw delete deny 23/tcp
   ```  

---

## 📝 Summary  
In this task, a firewall was configured using **UFW on Linux**. The process included:  

- Enabling UFW  
- Allowing SSH on port 22  
- Blocking Telnet on port 23 (insecure protocol)  
- Testing using Netcat  
- Removing the block rule to restore original configuration  

This demonstrates how **firewalls filter traffic** based on rules, strengthening system security by preventing unauthorized access while allowing legitimate connections.  

---

## 📂 Deliverables  
- Screenshot of firewall rules:  
  ```bash
  sudo ufw status numbered
  ```  
- Netcat test output:  
  ```bash
  nc -zv 127.0.0.1 23
  ```  
- Documentation of all commands used (above)  

---

✅ **End of Report**
