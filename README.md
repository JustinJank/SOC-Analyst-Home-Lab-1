# SOC-Analyst-Home-Lab-1

Home lab demonstrating Nmap scanning of a Windows 11 VM (RDP exposed) and analysis of Sysmon-generated system and IDS logs.

---

## Project Overview

This project documents the setup and execution of a foundational cybersecurity lab environment designed to simulate red team network scanning activities and blue team log analysis.

Two virtual machines were configured within an isolated virtual network:

- **Windows 11 VM** — Target system with Remote Desktop Protocol (RDP) enabled and Sysmon installed for detailed logging.  
- **Linux VM (Kali Linux)** — Attacker system running network scanning tools such as Nmap.

The lab demonstrates how network scanning techniques impact the target system and how defensive tools like Sysmon capture these activities in logs.

---

## Lab Setup and Configuration

- Installed Windows 11 and Kali Linux as virtual machines using VirtualBox.  
- Set static IPs and configured a private virtual network to isolate the lab environment.  
- Installed Sysmon on the Windows VM to monitor and log system events.  
- Installed penetration testing tools on the Linux VM via the command line interface (CLI).  
- Temporarily disabled Windows Firewall to allow scanning traffic.  
- Performed network scans (ping, port scans, and RDP port scans) from the Linux VM using Nmap.  
- Collected and analyzed detection logs on the Windows VM to identify attack signatures.

---

## Screenshots Overview

### Setup

<img src="screenshots/setup/Installing-Windows-11-on-VM.png" width="600" />
*Installing Windows 11 on the VM.*

<img src="screenshots/setup/Sysmon-Installation.png" width="600" />
*Installing Sysmon via PowerShell WebRequest.*

<img src="screenshots/setup/Pen-Tools-Download.png" width="600" />
*Downloading penetration testing tools on Kali Linux.*

---

### Troubleshooting

<img src="screenshots/troubleshooting/Static-IP-Conflict.png" width="600" />
*Resolving static IP conflicts.*

<img src="screenshots/troubleshooting/Kali-VM-Boot-Issue.png" width="600" />
*Kali VM boot and display issue.*

<img src="screenshots/troubleshooting/QOL-Fixes.png" width="600" />
*Quality-of-life adjustments for lab usability.*

---

### Scanning Results

<img src="screenshots/scans/Successful-Ping.png" width="600" />
*Successful ping between Windows 11 and Kali VMs.*

<img src="screenshots/scans/First-Port-Scan.png" width="600" />
*First successful port scan from Kali Linux.*

<img src="screenshots/scans/Nmap-RDP-Scan.png" width="600" />
*Nmap scan targeting the RDP port on Windows 11.*

---

### Log Analysis

<img src="screenshots/logs/Sysmon-Connection-Attempts.png" width="600" />
*Sysmon logs showing connection attempts.*

<img src="screenshots/logs/Sysmon-PowerShell-Status.png" width="600" />
*Sysmon running status in PowerShell.*

<img src="screenshots/logs/Sysmon-Results.png" width="600" />
*Captured Sysmon results in Windows VM.*

---

## How to Use This Repo

1. Review the screenshots for a visual walkthrough of the lab setup, execution, and troubleshooting.  
2. Read through the README to understand the project goals, methods, and results.  
3. Use this as a baseline for building your own cybersecurity lab environment or for learning red team vs blue team concepts.

---

## Next Steps

- Expand the lab by adding active defense tools such as additional IDS/IPS or EDR solutions.  
- Automate log collection and analysis with scripts or SIEM integration.  
- Perform more advanced penetration testing scenarios.  
- Expand the lab to conduct vulnerability testing and analysis.

---

## Contact / Contributions

This lab was created as a personal learning project. Contributions and feedback are welcome!

---

*Last updated: April 2026*
