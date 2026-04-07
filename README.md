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
- Set static IPs & configured a private virtual network to isolate the lab environment.  
- Installed Sysmon on the Windows VM to monitor and log system events.  
- Installed penetration testing tools on the Linux VM via CLI.  
- Temporarily disabled Windows Firewall to allow scanning traffic.  
- Performed network scans (ping, port scans, and RDP port scans) from the Linux VM using Nmap.  
- Collected and analyzed detection logs on the Windows VM to identify attack signatures.

---

## Screenshots Overview

### Setup

![W11 VM Install](screenshots/setup/W11-VM-Install.png)  
*Installing Windows 11 on the VM — first step to create target environment.*

![Sysmon Install PS](screenshots/setup/Sysmon-Install-PS.png)  
*Installing Sysmon via PowerShell to enable detailed event logging.*

![Sysmon Install Success](screenshots/setup/Sysmon-install-success-PS.png)  
*Sysmon installation verified successfully in PowerShell.*

![Pen Tools Install](screenshots/setup/Pen-Tools-Install-CLI.png)  
*Installing penetration testing tools on Kali Linux.*

![Internal Network Setup](screenshots/setup/Internal-Network-Setup.png)  
*Configuring isolated internal network so lab VMs can communicate without affecting the host.*

![Config Static IPv4](screenshots/setup/Config-Static-IPv4.png)  
*Configuring static IP addresses for both VMs for reliable communication.*

![QOL CLI Fixes](screenshots/setup/QOL-Disabling-Screen-Reader-CLI.png)  
*Quality-of-life adjustments in the VM CLI to improve usability.*

---

### Troubleshooting

![IP Conflict Error](screenshots/troubleshooting/Error-Creating-Static-IPs-Due-To-Conflicting-Addresses.png)  
*Resolving static IP conflicts during setup.*

![Failed Stealth Scans](screenshots/troubleshooting/Failed-Stealth-Port-Scans-after-firewall-enabled.png)  
*Initial stealth port scans failed due to Windows Firewall — demonstrates defensive control.*

![Kali Boot Fix](screenshots/troubleshooting/Kali-Breaks-change-boot-parameters-to-fix..png)  
*Adjusting Kali boot parameters to fix VM boot issues.*

![Kali Guest Display](screenshots/troubleshooting/Kali-VM-breaks-at-guest-display.png)  
*Fixing Kali VM display issues to ensure proper usability.*

![IPv4 Troubleshooting](screenshots/troubleshooting/ipv4-static-addressing-troubleshooting.png)  
*Troubleshooting static IPv4 addressing to ensure both VMs could communicate.*

---

### Scanning Results

![Successful Ping](screenshots/scans/Successful-Ping-Between-Machines-on-Internal-network.png)  
*Ping test confirming network connectivity between Windows and Linux VMs.*

![First Port Scan](screenshots/scans/successful-port-scan-RDP-windows.png)  
*First successful Nmap port scan targeting the RDP port — validates red team scanning activity.*

---

### Log Analysis

![Sysmon Connection Attempts](screenshots/logs/Sysmon-Log-Connection-Attempts.png)  
*Sysmon logs showing connection attempts from Linux VM — captures evidence of network scanning.*

![Sysmon Running in PS](screenshots/logs/Sysmon-Running-in-PS.png)  
*Sysmon running status verified in PowerShell.*

![Sysmon Results VBox](screenshots/logs/Sysmon-Results-VBox.png)  
*Detailed Sysmon log results in Windows VM — demonstrates defender perspective.*

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
