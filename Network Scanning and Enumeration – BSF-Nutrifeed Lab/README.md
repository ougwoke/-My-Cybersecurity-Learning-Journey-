**Network Reconnaissance & Vulnerability Scanning using Nmap**

**Overview**

This lab demonstrates the process of network reconnaissance and scanning within a controlled virtual environment. The objective was to identify active hosts, open ports, and running services in the BSF-Nutrifeed lab ecosystem.

Network scanning is a critical phase in cybersecurity assessments as it helps uncover potential attack surfaces and entry points that attackers may exploit.

**Objectives**

Identify devices on the network
Discover open ports and services
Perform service and version detection
Conduct deeper scans for vulnerability insights
Analyze potential security risks

**Tools Used**

Kali Linux
Nmap (Network Mapper)
VirtualBox Lab Environment (Windows 11, Wazuh, Metasploitable2)

**Lab Setup**

Machine	IP Address
Windows 11 VM	192.xxx.xx.xxx
Kali Linux VM	192.xxx.xx.xxx
Wazuh VM	192.xxx.xx.xxx
Metasploitable2	192.xxx.xx.xxx

**Scanning Activities**

1. Identify Local IP Address
ip a
2. Discover Active Hosts
nmap -sn 10.x.x.xx/24
3. Scan Target for Open Ports
nmap -sV 10.x.x.x
4. Perform Advanced Scan
nmap -A 10.x.x.x
5. Scan All Ports
nmap -p- 10.x.x.0/24

**Key Findings**

Open Ports & Services
Web services detected on port 8000
DNS service running on port 53
Multiple unknown and high-numbered ports open
Presence of uncommon/legacy services

**Identified Risks**

Exposure of web services (potential vulnerabilities)
DNS spoofing risk
Unidentified services may be outdated or insecure
High-numbered ports could indicate backdoors or misconfigurations

**Potential Entry Points**

Entry Point	Ports	Risk Level
Web Services	8000	High
DNS Service	53	High
Unknown Services	Multiple	High
Dynamic Ports	49xxx+	Medium–High

**Recommendations
**
Close unused ports
Configure firewall rules
Secure exposed services
Enforce strong authentication
Continuously monitor network activity

**Environment Update**

After integrating the Metasploitable2 VM and switching to a Host-Only Adapter network, IP addresses were reassigned. A follow-up scan was conducted to reflect the updated network structure.

**Key Takeaways**

Network scanning reveals critical security gaps
Misconfigured services significantly increase risk
Continuous monitoring is essential for security posture
