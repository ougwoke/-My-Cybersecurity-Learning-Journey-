
# Multi-LAN Network Architecture with DHCP Configuration (Cisco Packet Tracer)

## Overview
This project demonstrates the design and configuration of a small enterprise-style routed network using Cisco Packet Tracer. The lab focuses on interconnecting multiple LAN segments, implementing centralized DHCP services, and verifying end-to-end connectivity across routed networks.

This networking lab complements my SOC/SIEM projects by strengthening my foundational understanding of IP addressing, routing behavior, and network services that directly impact security monitoring and incident investigation.

---

## Objectives
- Design a multi-LAN network topology using routers, switches, and end devices
- Configure IP addressing and subnetting across multiple LAN segments
- Implement centralized DHCP services using a dedicated server
- Enable inter-network communication via routing
- Verify connectivity and troubleshoot common network issues

---

## Lab Architecture
**Devices used:**
- 2 Routers  
- 2 Switches  
- 3 PCs  
- 3 Laptops  
- 1 Dedicated DHCP Server  

**Topology highlights:**
- End devices distributed across multiple LANs
- Switches provide local connectivity
- Routers enable communication between LAN segments
- Centralized DHCP server dynamically assigns IP configuration

---

## Key Configurations
- Static IP addressing on routers and DHCP server
- DHCP pool configuration (network, subnet mask, default gateway)
- Correct interface selection and activation (`no shutdown`)
- End-device configuration via DHCP
- ICMP testing to validate end-to-end connectivity

---

## Validation & Testing
- Verified IP assignment via DHCP on all end devices
- Tested inter-LAN connectivity using `ping`
- Confirmed routing behavior between network segments
- Resolved initial DHCP assignment failures through troubleshooting

---

## Skills Demonstrated
- Network topology design
- TCP/IP and subnetting
- DHCP configuration and troubleshooting
- Routing fundamentals
- Network validation and documentation
- Cisco Packet Tracer hands-on experience

---

## Relevance to Security Operations
Understanding how networks assign IP addresses, route traffic, and segment hosts is critical for:
- SOC alert triage
- Log interpretation (source/destination IPs)
- Detecting misconfigurations and anomalous behavior
- Supporting incident investigations

---

## Documentation
This repository includes:
- Network topology screenshots
- Step-by-step configuration notes
- Connectivity test results

---

## Author
**Oliver Ugwoke**  
SOC Analyst | Junior Security Analyst  
GitHub: https://github.com/ougwoke  
LinkedIn: https://www.linkedin.com/in/oliver-ugwoke-266bb7187/
