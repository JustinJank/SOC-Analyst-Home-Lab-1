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

<img src="screenshots/setup/W11-VM-Install.png" width="600" />
*Installing Windows 11 on the VM — first step to create target environment.*


<img src="screenshots/setup/Sysmon-Install-PS.png" width="600" />
*Installing Sysmon via PowerShell to enable detailed event logging.*


<img src="screenshots/setup/Sysmon-install-success-PS.png" width="600" />
*Sysmon installation verified successfully in PowerShell.*


<img src="screenshots/setup/Pen-Tools-Install-CLI.png" width="600" />
*Installing penetration testing tools on Kali Linux.*


<img src="screenshots/setup/Internal-Network-Setup.png" width="600" />
*Configuring isolated internal network to ensure lab VMs can communicate without affecting the host network.*


<img src="screenshots/setup/Config-Static-IPv4.png" width="600" />
*Configuring static IP addresses for both VMs for reliable communication.*


<img src="screenshots/setup/QOL-Disabling-Screen-Reader-CLI.png" width="600" />
*Quality-of-life adjustments in the VM CLI to improve usability.*


---

### Troubleshooting

<img src="screenshots/troubleshooting/Error-Creating Static-IPs-Due-To-Conflicting-Addresses.png" width="600" />
*Resolving static IP conflicts during setup.*


<img src="screenshots/troubleshooting/Failed-Stealth Port-Scans-after-firewall-enabled.png" width="600" />
*Initial stealth port scans failed due to Windows Firewall — highlights importance of defensive settings.*


<img src="screenshots/troubleshooting/Kali-Breaks-change-boot-parameters-to-fix..png" width="600" />
*Adjusting Kali boot parameters to fix VM boot issues.*


<img src="screenshots/troubleshooting/Kali-VM-breaks-at-guest-display.png" width="600" />
*Fixing Kali VM display issues to ensure proper usability.*


<img src="screenshots/troubleshooting/ipv4-static-addressing-troubleshooting.png" width="600" />
*Troubleshooting IPv4 static addressing to ensure both VMs could communicate.*


---

### Scanning Results

<img src="screenshots/scans/Successful-Ping-Between-Machines-on-Internal-network.png" width="600" />
*Ping test confirming network connectivity between Windows and Linux VMs.*


<img src="screenshots/scans/First-successful-port-scan-after-enabling-RDP-on windows-machine.png" width="600" />
*First successful Nmap port scan targeting the Windows RDP port — validates red team scanning activity.*


---

### Log Analysis

<img src="screenshots/logs/Sysmon-Log-Connection-Attempts.png" width="600" />
*Sysmon logs showing connection attempts from Linux VM — captures evidence of network scanning.*


<img src="screenshots/logs/Sysmon-Running-in-PS.png" width="600" />
*Sysmon running status verified in PowerShell.*


<img src="screenshots/logs/Sysmon-Results-VBox.png" width="600" />
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
