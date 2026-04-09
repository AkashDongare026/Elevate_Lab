🛡️ Cyber Security Internship Task
🔍 Network Scanning using Nmap








📌 Overview

This project demonstrates how to perform network scanning using Nmap on a Linux system.
The goal is to identify active devices, detect open ports, analyze running services, and evaluate potential security risks in a local network.

🎯 Objectives

✔ Scan the local network to find active hosts
✔ Identify open TCP ports
✔ Detect services running on those ports
✔ Analyze possible security vulnerabilities
✔ Save scan results for reporting

🛠️ Tools & Technologies
🐧 Operating System: Linux (Ubuntu)
🔍 Tool: Nmap
📡 Optional Tool: Wireshark
🌐 Network Range
192.168.1.0/24
⚙️ Command Used
sudo nmap -sS 192.168.1.0/24 -oN scan.txt
📊 Scan Results Summary
🖥️ Host: 192.168.1.1 (Gateway / Router)
Open Ports:
22   → SSH
53   → DNS
80   → HTTP
1900 → UPnP
🖥️ Host: 192.168.1.100 (Local Machine)
Open Ports:
22   → SSH
9200 → API / Elasticsearch
🔎 Services Identified
Port	Service	Description
22	SSH	Remote login
53	DNS	Domain resolution
80	HTTP	Web interface
1900	UPnP	Device discovery
9200	API	Elasticsearch / Web service
⚠️ Security Risks

🚨 SSH (Port 22)

Vulnerable to brute-force attacks

🚨 HTTP (Port 80)

Data is not encrypted

🚨 UPnP (Port 1900)

Can expose devices externally

🚨 Port 9200

Possible data exposure if unsecured
🔐 Recommended Mitigations
🔑 Use strong passwords & SSH key authentication
🚫 Disable root login for SSH
🔒 Use HTTPS instead of HTTP
⚙️ Disable UPnP if not required
🧱 Apply firewall rules
🔐 Enable authentication for services
📁 Output


🚀 How to Run
# Install Nmap
sudo apt update
sudo apt install nmap

# Run Scan
sudo nmap -sS 192.168.1.0/24 -oN scan.txt
✅ Conclusion

The Nmap scan successfully identified active hosts and open ports in the network.
Security risks were analyzed, and mitigation strategies were suggested to improve network security.
