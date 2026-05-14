**End-to-End Incident Response & Attack Simulation Lab**

**Overview**

This project demonstrates a comprehensive security simulation within a controlled lab environment. The primary goal was to emulate real-world cyberattack scenarios covering reconnaissance, exploitation, and detection—while implementing defensive controls to mitigate the threats.

**Lab Architecture**

The environment was structured using three main systems to simulate an enterprise network: 
      Attacker Node: Kali Linux 
      Target Node: Ubuntu Server hosting DVWA and a Cowrie Honeypot. 
      Monitoring Node: Wazuh SIEM for log aggregation and alerting. 

**Technical Toolstack**
     
      Offensive: Kali Linux, Nmap, Metasploit, Hydra. 
      Defensive: ModSecurity (WAF), UFW Firewall. 
      Monitoring/SIEM: Wazuh. 
      Deception: Cowrie Honeypot. 
      Target: Damn Vulnerable Web Application (DVWA). 

**Execution Phases**

1. Attack Phase (Exploitation)
      Reconnaissance: Conducted service and version detection via Nmap, identifying open HTTP (80) and SSH-like (2222) ports. 
      Web Exploitation: Manually executed SQL Injection, Cross-Site Scripting (XSS), and Command Injection. 
      Reverse Shell: Gained access to the target using the Metasploit Web Delivery exploit with a Python Meterpreter payload. 

2. Detection & Monitoring
      SIEM Alerts: Wazuh successfully alerted on port scanning, brute-force attempts via Hydra, and suspicious command injection requests. 
      Log Correlation: Integrated interaction logs from the Cowrie Honeypot to identify malicious connection patterns on port 2222. 

3. Response & Mitigation
      WAF Implementation: Configured ModSecurity rules to filter and block malicious HTTP requests, specifically targeting SQLi, XSS, and command injection patterns. 
      Network Hardening: Utilized the UFW Firewall to restrict the attack surface, allowing only necessary HTTP traffic and blocking unauthorized access to the honeypot port. 

**Lessons Learned**

Vulnerability Management: The simulation highlighted critical risks associated with weak input validation, misconfigured security settings, and exposed services. 
      Defense-in-Depth: Implementing layered security (SIEM + WAF + Firewall) significantly improved the overall detection and mitigation posture of the environment. 
      
    • Continuous Improvement: Future iterations should focus on enforcing strong authentication policies and regular system hardening. 
