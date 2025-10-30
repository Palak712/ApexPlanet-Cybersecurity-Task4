# ApexPlanet-Cybersecurity-Task4
Network Security &amp; Vulnerability Assessment  This task focuses on understanding and performing network scanning, service enumeration, and vulnerability analysis using industry-standard tools in a controlled lab environment.

## 📌 Overview
This repository contains my work for *Task 4: Network Security & Vulnerability Assessment*.  
All activities were performed in an isolated virtual lab (Kali Linux as attacker → target VM) to safely practice network discovery, service enumeration, vulnerability scanning, and report interpretation.

*Primary goals*
- Discover live hosts and network topology
- Enumerate open ports and services
- Perform vulnerability scans and interpret results
- Validate findings manually and propose mitigations

*Tools used:* Kali Linux · Nmap · Zenmap · OpenVAS / Nessus · Wireshark · netdiscover · xsltproc

## 🧭 Lab Topology (example)
- *Kali Linux (Attacker)* — 192.168.56.103  
- *Target VM (Victim)* — 192.168.56.101 
- *Network:* VirtualBox Host-Only (isolated)


---

## 🔧 Setup & prerequisites
1. Install VirtualBox / VMware and import or install target VM (Metasploitable, Ubuntu + services, etc.).  
2. Install Kali or use an existing Kali VM.  
3. Make sure both VMs share the same Host-Only network.  
4. Install OpenVAS/GVM on Kali: sudo gvm-setup / sudo gvm-start and access the web UI at https://127.0.0.1:9392/.

---

## 🛠 Key commands (copy & run)

## Linkedin Video Link
  https://www.linkedin.com/posts/palak-baranwal-a98145337_cybersecurity-networksecurity-vulnerabilityassessment-activity-7389618305441091584-Jz1h?utm_source=social_share_send&utm_medium=android_app&rcm=ACoAAFSPZ9QBM7MH4wKOnhLjjQttu_AWlDqDMA0&utm_campaign=copy_link

### Host discovery
```bash
# ARP/host discovery
sudo netdiscover -r 192.168.56.0/24
# ICMP ping sweep
sudo nmap -sn 192.168.56.0/24 -oN scans/host_discovery.txt

