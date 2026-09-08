# Hybrid-Multi-Interface-IDS-IPS
Hybrid Multi-Interface IDS/IPS platform using Suricata, Python, behavioral analysis, real-time alerts, automated IP blocking, and threat intelligence dashboard.

# 🛡️Hybrid Multi-Interface IDS/IPS Platform Using Suricata

## 📌 Project Overview

This project implements a hybrid **Intrusion Detection and Prevention System (IDS/IPS)** using **Suricata, Python, Linux firewall tools, and a Flask-based dashboard**.

The platform is designed to monitor network traffic across multiple interfaces, detect suspicious network activity using custom Suricata rules, analyze behavioral patterns, classify threats based on their severity, generate real-time email alerts, and automatically block malicious source IP addresses.

The project also extends traditional signature-based detection with **behavioral analysis of file uploads and repeated network activity**, providing a more complete view of potential threats.

The entire system was implemented and tested in a controlled laboratory environment using simulated attack scenarios.

---

## 🎯 Project Objectives

- Monitor network traffic across different network interfaces.
- Separate and analyze LAN and WAN traffic.
- Detect ICMP, HTTP, SYN flood, and network scanning activities.
- Detect repeated and abnormal traffic patterns.
- Analyze uploaded files based on file type, size, and repetition.
- Classify detected activities according to threat severity.
- Calculate threat scores for suspicious behavior.
- Generate real-time email notifications for security events.
- Automatically block malicious IP addresses using `iptables`.
- Maintain attack timelines and security event logs.
- Provide centralized visualization through a Threat Intelligence Dashboard.
- Demonstrate the integration of IDS detection with IPS prevention.

---

## 🔍 Key Features

### 🌐 Multi-Interface Monitoring

The platform supports monitoring of different network interfaces and separates LAN and WAN traffic for better visibility and analysis.

### 🚨 Signature-Based Detection

Suricata is configured with custom rules to detect activities such as:

- ICMP traffic
- HTTP requests
- ICMP Flood
- HTTP Flood
- SYN Flood
- Nmap scanning

### 🧠 Behavioral Analysis

A Python-based behavior analyzer monitors security events and identifies suspicious patterns that may not be captured by simple signature rules.

The analyzer evaluates factors such as:

- Repeated requests
- Upload frequency
- File extensions
- File size
- Suspicious executable or script files

### 📊 Threat Scoring

Detected activities are assigned threat scores and classified into different severity levels such as:

- Normal
- Suspicious
- Medium Threat
- High Threat

### 📧 Real-Time Alerts

The system can send email notifications when suspicious activity reaches defined threat levels.

Alerts include information such as:

- Source IP
- Threat type
- Severity
- Timestamp
- Event details

### 🛑 Automated IP Blocking

When a malicious activity reaches the required threat level, the system can automatically trigger an `iptables` rule to block the source IP.

This connects the detection layer with the prevention layer of the IDS/IPS.

### 📈 Threat Intelligence Dashboard

A Flask-based dashboard provides centralized visibility into:

- Detected threats
- Security events
- Attack timeline
- Blocked IP addresses
- Threat information

---

## 🧪 Testing Scenarios

The platform was tested using several controlled scenarios, including:

- ICMP Flood
- HTTP Flood
- Nmap Scanning
- Repeated HTTP Requests
- Normal File Uploads
- Executable File Uploads
- PHP/Script File Uploads
- Large File Uploads
- Repeated Upload Attempts
- Suspicious Archive Detection

These tests were used to validate detection, behavioral analysis, alerting, scoring, and automated blocking.

---

## 🔄 System Workflow

```text
Network Traffic
       ↓
Multi-Interface Monitoring
       ↓
Suricata Detection
       ↓
Security Event Logs
       ↓
Behavioral Analysis
       ↓
Threat Scoring & Classification
       ↓
   ┌───────────────┐
   ↓               ↓
Email Alerts    IP Blocking
                    ↓
                 iptables
   └───────┬───────┘
           ↓
Threat Intelligence Dashboard
```

---

## 🛠️ Technologies

| Technology | Purpose |
|------------|---------|
| 🛡️ Suricata | Network IDS/IPS and signature-based detection |
| 🐍 Python 3 | Behavioral analysis, automation, scoring, and dashboard |
| 🔥 iptables | Automated firewall-based IP blocking |
| 🌐 Flask | Threat intelligence dashboard |
| 💻 Linux | Monitoring and security environment |
| 📡 tcpdump | Network traffic verification |
| 🔎 Nmap | Network scanning test generation |
| 🖥️ Bash | Firewall and system automation |
| 📧 Gmail/SMTP | Real-time security alerts |
| 📶 Aircrack-ng | Wireless interface testing |

---

## 📂 Project Files

### 📄 Presentation
`Hybrid-Multi-Interface-IDSIPS-Platform-Using-Suricata.pptx`

Project presentation explaining the system design, implementation, testing, and results.

### 📑 Project Report
`Suricata_IDS_IPS_Results_Report.pdf`

Detailed documentation of the experiment, including configuration steps, testing scenarios, screenshots, detection results, alerting, IP blocking, and dashboard implementation.

### 💻 Project Files

The project implementation contains:

- `behavior.rules` — Behavioral Suricata detection rules.
- `lan.rules` — LAN monitoring rules.
- `wan.rules` — WAN monitoring rules.
- `behavior_analyzer.py` — Behavioral analysis and threat classification.
- `subscribe_server.py` — Supporting server component for event handling.
- `threat_dashboard.py` — Flask-based threat intelligence dashboard.
- `watch_alerts.py` — Alert monitoring component.
- `block_ip.sh` — Automated IP blocking using iptables.
- `firewall_subscribers.sh` — Firewall-related automation.

---

## 📊 Results

The implemented platform successfully demonstrated:

✅ Multi-interface network monitoring  
✅ LAN and WAN traffic detection  
✅ ICMP and HTTP detection  
✅ Flood and scanning detection  
✅ Behavioral file analysis  
✅ Threat scoring and classification  
✅ Real-time email alerts  
✅ Automated malicious IP blocking  
✅ Attack timeline logging  
✅ Centralized threat intelligence dashboard  

The experiments demonstrate how the platform can move from **detecting suspicious activity to analyzing, alerting, and actively preventing further access**.

## Author

 **Tamam Dreat**
 
 **Cybersecurity Student**
 
**An-Najah National University**
