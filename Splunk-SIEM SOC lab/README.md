Splunk SIEM SOC Lab: Endpoint Monitoring & Log Analysis

Objective

The primary objective of this project was to build a functional, end-to-end Splunk-based SIEM lab to simulate SOC (Security Operations Center) analysis. The environment was designed to ingest, parse, and analyze various telemetry sources, including Windows Security events, Sysmon, and DNS/HTTP logs, to identify potential security threats.

Lab Architecture

    • Host OS: Kali Linux 
    • Guest OS: Windows 11 VM (Target Endpoint) 
    • SIEM Platform: Splunk Enterprise 
    • Data Collection: Splunk Universal Forwarder (UF) and Sysmon 

Key Activities & Technical Skills

    • SIEM Administration: Installed and configured Splunk Enterprise to act as a central receiver on port 9997.
    • Endpoint Telemetry: Deployed Sysmon and the Splunk Universal Forwarder on a Windows 11 endpoint.
    • Log Forwarding Configuration: Manually configured inputs.conf to streamline the collection of WinEventLog:Security and Sysmon Operational logs.
    • Threat Hunting with SPL: Developed custom Splunk Search Processing Language (SPL) queries to identify specific security events, such as:
        ◦ Failed Logins (EventCode 4625): Investigating potential brute-force attempts.
        ◦ Asset Monitoring: Summarizing event distributions across hosts.
    • Log Parsing & Field Extraction:
        ◦ Ingested unstructured DNS logs into Splunk.
        ◦ Utilized Regular Expressions (Regex) to perform manual field extractions for source/destination IPs and ports, transforming raw data into actionable intelligence.

Data Sources Ingested

    • Windows Security Events 
    • System Monitor (Sysmon) 
    • DNS/HTTP Logs 
