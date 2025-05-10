# Strengthened-Security-on-Metasploitable-3
A comprehensive system hardening project on Metasploitable 3 using Wazuh SIEM, vulnerability scanning (OpenVAS, Nessus), and remediation of critical security flaws.
# System Hardening – Metasploitable 3 (Wazuh Implementation & Vulnerability Remediation)

## 🔐 Overview
This repository presents a cybersecurity hardening project focused on improving the security posture of **Metasploitable 3**, a vulnerable virtual machine. The task was undertaken for the course **Hardening Modern Operating Systems and Applications**. It involved identifying vulnerabilities, implementing fixes, setting up **Wazuh SIEM/XDR**, simulating attacks, and monitoring traffic using Wireshark.

## 🧰 Tools & Technologies Used
- **SIEM/XDR**: Wazuh Server & Agent
- **Scanning**: Nmap, OpenVAS, Nessus, Nikto, OWASP ZAP
- **Attack Simulation**: Metasploit, SQL Injection, John the Ripper
- **Monitoring**: Wireshark
- **OS**: Metasploitable 3 (Ubuntu 14.04), Kali Linux, Windows 11

## 🧪 Project Scope
- Deployed Wazuh server and agents across VMs for real-time monitoring
- Identified and remediated **4 major vulnerabilities**:
  - **Port 21 (FTP)** – ProFTPD mod_copy RCE (`CVE-2015-3306`)
  - **Port 22 (SSH)** – Default root credentials (`CVE-2024-22902`)
  - **Port 80 (HTTP)** – SQL Injection on Drupal CMS (`CVE-2014-3704`)
  - **Port 631 (IPP)** – Weak cipher suite (SWEET32, `CVE-2016-2183`)
- Converted FTP to SFTP with group/user restrictions
- Enforced HTTPS with Apache and SSL certificates
- Simulated SQL injection attacks and monitored using Wireshark
- Blocked vulnerable services (e.g., CUPS on port 631) via firewall rules

## 🔄 Key Improvements
| Vulnerability | Remediation |
|---------------|-------------|
| FTP (Port 21) | Converted to SFTP and disabled ProFTPD |
| SSH (Port 22) | Limited access to specific IPs, changed default credentials |
| HTTP (Port 80) | Configured HTTPS, implemented SQLi protection |
| IPP (Port 631) | Blocked traffic via firewall after conf fix failed |

## 📄 Files in This Repo
- `Strengthened Security on Metasploitable 3.pdf`: Full hardening and incident response report
- `README.md`: Summary and highlights of the project

## 📌 Disclaimer
This project was conducted in a virtual lab environment for academic purposes only. All tools and simulations were run under controlled conditions.

---

> 📚 *Project by Alcides Gomez, Leoj Muyco, Luís Landa, and Mohammad Kaif for Professor Travis Czech at Cambrian College.*
