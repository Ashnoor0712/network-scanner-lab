# Network Scanner Lab (Nmap)

## Overview

This project demonstrates a hands-on cybersecurity lab focused on network reconnaissance using Nmap. The objective was to simulate how an attacker or security analyst gathers information about systems on a network, including identifying active hosts, open ports, and running services.

By performing structured scans in a controlled virtual environment, this project highlights how seemingly small pieces of information can expose critical details about a system’s security posture.

---

## Objectives

* Identify active devices on a network
* Perform port scanning on a target system
* Detect running services on open ports
* Analyze potential security risks from exposed services
* Understand how attackers perform reconnaissance

---

## Tools Used

* Nmap (Network scanning tool)
* Ubuntu (Virtual Machine)
* VirtualBox (Virtualization platform)

---

## Lab Environment

* OS: Ubuntu (Virtual Machine)
* Network Range: 10.0.2.0/24
* Target System: 10.0.2.15
* Setup: Isolated virtual lab environment for safe testing

---

## Methodology

### 1. Host Discovery

Command:
nmap -sn 10.0.2.0/24

Purpose:
Used to identify active devices on the network without scanning ports.

Outcome:
Discovered available hosts within the subnet.

---

### 2. Port Scanning

Command:
nmap 10.0.2.15

Purpose:
Performed a basic scan to identify open ports on the target system.

Outcome:
Revealed which ports were accessible and potentially exposed.

---

### 3. Service Detection

Command:
nmap -sV 10.0.2.15

Purpose:
Identified services running on open ports along with version information.

Outcome:
Provided insight into what software and services were active.

---

### 4. Advanced Scanning (Enhanced Analysis)

Command:
nmap -A 10.0.2.15

Purpose:
Enabled aggressive scanning including OS detection, version detection, and script scanning.

---

Command:
nmap -O 10.0.2.15

Purpose:
Attempted to identify the operating system of the target machine.

---

Command:
nmap --script vuln 10.0.2.15

Purpose:
Scanned for known vulnerabilities using Nmap’s scripting engine.

---

## Key Findings

* Only a limited number of ports were open on the system
* Services running on open ports were identifiable through version detection
* The system had a relatively small attack surface
* No critical vulnerabilities were detected in basic scans (if applicable)

---

## Security Analysis

Open ports act as potential entry points for attackers. Even a single exposed service can be exploited if it is misconfigured or outdated.

Examples of common risks:

* Port 22 (SSH): Brute-force login attempts
* Port 80 (HTTP): Unencrypted communication vulnerable to interception
* Port 443 (HTTPS): Secure but still exposed to web-based attacks
* Unknown services: May contain vulnerabilities if not patched

This demonstrates how attackers can quickly map a system and identify possible weaknesses.

---

## Risk Assessment

* Low number of open ports reduces exposure
* Identified services may still pose risks if not regularly updated
* Lack of firewall restrictions could allow unauthorized access

---

## Mitigation Recommendations

* Close all unnecessary ports
* Use firewall rules to restrict access (e.g., allow only trusted IPs)
* Regularly update and patch services
* Disable unused services
* Implement intrusion detection systems (IDS)

---

## Conclusion

This project demonstrates how network scanning can reveal critical information about a system in just a few minutes. Even simple reconnaissance techniques can expose valuable details that attackers can exploit.

By understanding these techniques, security professionals can better defend systems by minimizing exposure, monitoring services, and applying proactive security measures.

---

## Future Improvements

* Integrate Wireshark for packet-level analysis
* Perform scans on multiple machines for comparison
* Automate scanning using scripts
* Combine with vulnerability scanners like Nessus or OpenVAS

---

## Detailed Explanation 

This project reflects the reconnaissance phase of a cybersecurity assessment. Before any deeper testing can happen, it is important to understand what systems are active, what ports are open, and what services are exposed to the network.
The host discovery step helps identify which devices are reachable on the local network. This is useful because it shows what systems are present before focusing on one specific target.
The port scan then reveals which communication channels are open on the target machine. Since services listen on ports, this gives an early view of the machine’s attack surface.
The service detection step provides additional context by identifying what software may be running behind those open ports. From a defensive point of view, this helps determine whether exposed services are expected, necessary, and safely configured.
By performing this lab in a controlled virtual environment, I gained practical experience with basic network reconnaissance and a better understanding of how systems expose information on a network.

