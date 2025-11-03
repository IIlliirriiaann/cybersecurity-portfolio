# Nmap Network Scanning Lab

## Overview
This lab explores the capabilities of **Nmap**, a powerful network scanning tool, to analyze and identify vulnerabilities in target systems. The project focuses on **service enumeration, OS detection, and script-based vulnerability assessment** using Nmap's advanced features.

---

## Objectives
- Perform **service version detection** on vulnerable machines.
- Identify **operating systems** running on target machines.
- Utilize **Nmap Scripting Engine (NSE)** to automate vulnerability detection and information gathering.

---

## Methodology

### 1. Service Version Detection
Scanned **Metasploitable 2** and **Metasploitable 3** (a vulnerable Windows machine) using the `-sV` flag to enumerate service versions.

**Example Output:**
![Metasploitable 2 Service Scan]([screenshots/SV_meta2.png])
![Metasploitable 3 Service Scan]([screenshots/SV_meta3.png])

---

### 2. Operating System Detection
Used the `-A` flag to gather comprehensive information about the target systems, including OS detection.

**Example Output:**
![Nmap -A Flag Scan]([screenshots/A_flag.png])

For focused OS detection, the `-O` flag was used:

![Nmap -O Flag Scan]([screenshots/0_flag.png])

---

### 3. Nmap Scripting Engine (NSE)
Leveraged NSE scripts to enhance scanning capabilities:

- **SMB Enumeration:** Identified shared resources and vulnerabilities.
  ![SMB Enumeration Script]([screenshots/script_OS])

- **Anonymous FTP Login:** Detected misconfigured FTP services allowing anonymous access.
  ![FTP Script Output]([screenshots/script_FTP])

- **EternalBlue Vulnerability (MS17-010):** Confirmed the presence of the critical vulnerability on the Windows machine.
  ![EternalBlue Script Output]([screenshots/script_EternalBlue])

- **HTTP Directory Enumeration:** Enumerated directories on a web server.
  ![HTTP Script Output]([screenshots/script_HTTP])

---

## Key Findings
- **Service Versions:** Identified outdated and vulnerable services running on both Metasploitable 2 and 3.
- **OS Detection:** Successfully determined the operating systems of the target machines.
- **Vulnerabilities:** Discovered critical vulnerabilities, such as **EternalBlue (MS17-010)** and **anonymous FTP access**, which could be exploited by attackers. Found multiple **HTTP subfolders**, some of which may be interesting.

---

## Skills Demonstrated
- **Network Scanning:** Proficient use of Nmap for service and OS detection.
- **Vulnerability Assessment:** Automated detection of vulnerabilities using NSE scripts.
- **Security Analysis:** Ability to interpret scan results and identify potential security risks.

---

## Tools Used
- **Nmap**
- **Metasploitable 2 & 3** (Vulnerable VMs for testing)

---
