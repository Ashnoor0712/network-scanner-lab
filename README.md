# Cybersecurity Lab Project — Network Scanning

## Project Overview
This project demonstrates basic network reconnaissance using Nmap in a controlled virtual lab environment.

The goal was to identify active hosts on a network and analyze open ports and running services.

---

## Lab Setup
- Environment: VirtualBox (Ubuntu VM)
- Network Type: NAT (isolated network)
- IP Address: 10.0.2.15
- Network Range: 10.0.2.0/24

---

## Tools Used
- Nmap

---

## Steps Performed

### 1. Identify Network Information
Command:
ip a

Purpose:
To determine the system's IP address and network range.

---

### 2. Network Scan (Host Discovery)
Command:
nmap -sn 10.0.2.0/24

Result:
- Only one host detected (10.0.2.15)
- No additional devices found on the network

---

### 3. Port Scan
Command:
nmap 10.0.2.15

Result:
- All 1000 ports are closed
- No open ports detected

---

### 4. Service Detection
Command:
nmap -sV 10.0.2.15

Result:
- No services detected
- No active listening ports

---

## Key Learnings
- How to identify network range and IP configuration
- How to perform host discovery using Nmap
- Understanding open vs closed ports
- Importance of minimizing attack surface

---

## Conclusion
The system is active but does not expose any network services, indicating a secure default configuration with minimal attack surface.
