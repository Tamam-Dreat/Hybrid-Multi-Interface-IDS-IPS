# Hybrid-Multi-Interface-IDS-IPS
Hybrid Multi-Interface IDS/IPS platform using Suricata, Python, behavioral analysis, real-time alerts, automated IP blocking, and threat intelligence dashboard.
# Hybrid Multi-Interface IDS/IPS Platform Using Suricata

## Project Overview

This project implements a hybrid Intrusion Detection and Prevention System (IDS/IPS) using Suricata, Python, and iptables.

The platform extends traditional network monitoring by supporting multiple interfaces for LAN, WAN, and wireless monitoring. It combines signature-based detection with behavioral analysis, threat scoring, real-time email alerts, automated IP blocking, and a centralized threat intelligence dashboard.

The project was developed and tested in a controlled laboratory environment using custom Suricata rules and simulated attack scenarios.

---

## Project Objectives

- Monitor network traffic across multiple interfaces.
- Detect ICMP, HTTP, flooding, scanning, and suspicious file activities.
- Analyze repeated and abnormal behaviors beyond static signatures.
- Assign threat scores based on detected activities.
- Generate real-time alerts for security events.
- Automatically block malicious IP addresses using iptables.
- Monitor wireless traffic using a dedicated WiFi interface.
- Provide centralized visibility through a threat intelligence dashboard.

---

## Project Modules

### 1. Multi-Interface Network Monitoring
Monitor LAN, WAN, and wireless traffic using separate network interfaces to provide broader network visibility.

### 2. Suricata Detection & Custom Rules
Use Suricata with custom rules to detect ICMP, HTTP, flooding, SYN, and network scanning activities.

### 3. Behavioral Analysis
Analyze traffic and file-upload behavior to identify repeated requests, suspicious files, large uploads, and abnormal activity.

### 4. Threat Scoring & Classification
Assign dynamic threat scores to events and classify them as Normal, Suspicious, Medium Threat, or High Threat.

### 5. Real-Time Email Alerts
Send email notifications when detected activities reach defined threat levels.

### 6. Automated IPS Blocking
Extract suspicious source IP addresses and automatically block them using iptables.

### 7. Threat Intelligence Dashboard
Provide a centralized Flask-based dashboard for viewing detected threats, attack timelines, and blocked IP addresses.

---

## Technologies

- Suricata
- Python 3
- Flask
- iptables
- Bash
- Aircrack-ng
- Linux
- USB WiFi Adapter

---

## Project Files

- 📄 **Presentation:** `Presentation.pdf`
- 📄 **Project Report:** `Project-Report.docx`
- 📁 **Project Files:** `Project-Files/`

The project files include Suricata rules, Python analysis scripts, firewall scripts, dashboard components, and supporting screenshots.

## Author

 **Tamam Dreat**
 
 **Cybersecurity Student**
 
**An-Najah National University**
