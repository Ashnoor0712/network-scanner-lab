# Network Scanner Lab (Nmap)

## Overview
This project demonstrates a hands-on cybersecurity lab where I used Nmap to perform network scanning, host discovery, and service enumeration in a controlled environment.

The goal was to understand how systems appear on a network and what information can be gathered through basic reconnaissance techniques.

## Objectives
- Identify active devices on a network
- Perform port scanning on a target system
- Detect running services on open ports
- Understand how network exposure can be analyzed

## Tools Used
- Nmap
- Ubuntu (Virtual Machine)
- VirtualBox

## Lab Environment
- OS: Ubuntu (Virtual Machine)
- Network Range: 10.0.2.0/24
- Target System: Local VM (10.0.2.15)

## Method

### Host Discovery
nmap -sn 10.0.2.0/24

Used to identify which devices were active on the network.

### Port Scanning
nmap 10.0.2.15
Scanned the target machine for open ports.

### Service Detection
nmap -sV 10.0.2.15
Detected services running on open ports.

## Key Findings
- Only a small number of ports were open on the system
- Most services were not externally exposed
- The system had minimal visible attack surface

## Security Insights
- Even simple scans can reveal important system details
- Open ports and services provide entry points for attackers
- Limiting exposed services reduces security risk

## Resume-Ready Summary
Performed network reconnaissance using Nmap in a virtual lab environment to identify active hosts, scan open ports, and detect running services, gaining hands-on experience in network security analysis.
