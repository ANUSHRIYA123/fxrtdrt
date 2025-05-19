🛡 Network Penetration Testing with Real-World Exploits and Security Remediation

This project simulates real-world network attacks and defense strategies using Kali Linux as the attacker machine and Metasploitable as the target. It includes scanning, enumeration, exploitation, password cracking, and remediation — all performed in a controlled lab environment for ethical learning purposes.

🎯 Objectives
Understand and simulate real-world network attacks
Perform scanning, enumeration, and exploitation using tools like Nmap and Metasploit
Crack Linux password hashes using John the Ripper
Identify outdated services and recommend security remediations

💻 Lab Setup

🖥 Operating Systems
Kali Linux – Attacker Machine
Metasploitable 2 – Target Machine

🛠 Tools Used
Nmap – For network scanning,Port discovery, OS detection, and service enumeration 
Metasploit framework –  For Exploitation known vulnerabilities in services 
John the Ripper – Password hash cracking
Linux built-in commands – user management and enumeration

🚀 Tasks Performed
🔍 Network Scanning
nmap -v IP – Basic network scan
nmap -v -p- IP – Full port scan
nmap -sV IP – Service version detection
nmap -O IP – OS detection

🔐 Hidden Ports Discovered
Ports like 8787, 36588, 53204, etc., found through full port scans.

📡 Enumeration
OS: Linux 2.6.x (Metasploitable)
Open services: vsftpd, OpenSSH, Apache, MySQL, Samba, etc.
Vulnerable ports: 21 (FTP), 445 (SMB), 512–514 (R Services)

💥 Exploitation
vsftpd 2.3.4 backdoor
SMB 3.0.20-Debian using Metasploit
Rexec/Rlogin/Rsh services using script-based vulnerabilities

👤 Privilege Escalation
Created user anushriya with root permissions
Extracted and cracked password hash using John the Ripper


🔧 Remediation Steps
Service	Vulnerability	Fix
vsftpd	Backdoor (CVE-2011-2523)	Upgrade to 3.0.5 / use SFTP

R Services	Plaintext creds (CVE-1999-0651)	Disable & use SSH instead

📚 Major Learning
Through this project, I learned how to create and manage users in Linux, analyze system files, crack password hashes, and detect services using Nmap. I practiced using commands like nmap -sV, nmap -O, and john to identify system weaknesses. I also understood how outdated services like FTP

and R services pose serious security risks and how to patch or replace them.

⚠ Disclaimer
This project is for educational purposes only. All activities were performed in a safe, offline lab environment. Do not attempt these techniques on real networks without explicit permissions.

📎 References
CVE-2011-2523
Metasploit Documentation
John the Ripper
Apache Vulnerabilities