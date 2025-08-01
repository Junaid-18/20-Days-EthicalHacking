# 🔐 30 Days of Ethical Hacking 

Welcome to **Day 1** of my **30-Day Ethical Hacking Challenge**! This journey documents my daily learning and hands-on progress in cybersecurity using Kali Linux.

---

## 🚀 Day 1 Topics:
- ✅ Installing VirtualBox
- ✅ Downloading & Installing Kali Linux
- ✅ Configuring VM for smooth performance
- ✅ Understanding key hacking terms

---

## 📥 Step 1: Install VirtualBox

1. Visit: [https://www.virtualbox.org/](https://www.virtualbox.org/)
2. Click "Download VirtualBox".
3. Choose your platform (Windows, macOS, Linux).
4. Install it like any other software.

---

## 🌐 Step 2: Download Kali Linux ISO

1. Go to: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)
2. Scroll to "Kali Linux ISO".
3. Download the **64-bit (amd64) XFCE** ISO for lightweight performance.
   - Example: `kali-linux-2024.2-installer-amd64.iso`

---

## 🖥️ Step 3: Set Up Kali VM in VirtualBox

### ✅ Recommended Settings:
| Setting           | Value                |
|------------------|----------------------|
| Name              | Kali Linux           |
| Type              | Linux                |
| Version           | Debian (64-bit)      |
| RAM               | 2560 MB (2.5 GB)     |
| CPU Cores         | 2                    |
| Video Memory      | 128 MB (max)         |
| Graphics          | Enable 3D Acceleration |
| Storage           | 20 GB+ (dynamic)     |

---



## 📄 Notes PDF
See [`Day1.docx`](./Day1.docx) for:
- Definitions: White Hat, Black Hat, Pen Testing
- Installation summary
- System requirements
- Outcome of setup

---

## 📌 What I Learned
- Difference between hacker types
- How to install a secure Linux OS for pen testing
- System tuning for virtualization

---


# 🛡️ Day 2: Cyber Kill Chain, Reconnaissance & Ethical Hacking Phases

## 📌 1. Cyber Kill Chain Methodology

- **Reconnaissance**: Attacker gathers information about the target.
- **Weaponization**: Creation of malicious payload using collected data.
- **Delivery**: Sending the payload (email, USB, website).
- **Exploitation**: Triggering the payload using a system vulnerability.
- **Installation**: Installing malware/backdoor on the system.
- **Command & Control (C2)**: Remote communication/control by attacker.
- **Actions on Objectives**: Final goals like data theft or system takeover.

---

## 🔍 2. Introduction to Reconnaissance

Reconnaissance is the first step in both the Cyber Kill Chain and Ethical Hacking. It involves gathering intel about the target system.

**Types of Reconnaissance:**
- **Passive Reconnaissance**: No direct interaction (e.g., WHOIS, Google Dorks).
- **Active Reconnaissance**: Direct probing/scanning (e.g., Nmap, traceroute).

---

## 🆚 3. Passive vs Active Reconnaissance

| Feature             | Passive Reconnaissance         | Active Reconnaissance            |
|---------------------|--------------------------------|----------------------------------|
| **Definition**      | No direct interaction          | Direct interaction with target   |
| **Detection Risk**  | Low                            | High                             |
| **Tools**           | Google Dorking, Whois, Shodan  | Nmap, Netcat, Traceroute         |
| **Data Gathered**   | Public Info (DNS, Email, etc.) | Ports, OS, Services              |

---

## ⚔️ 4. 5 Phases of Ethical Hacking

| Phase               | Description                                                       | Techniques Used                                                        |
|---------------------|-------------------------------------------------------------------|------------------------------------------------------------------------|
| **Reconnaissance**  | Gathering info about the target system.                          | Google Dorking, WHOIS, DNS enum, Social Engineering                    |
| **Scanning**        | Identifying vulnerabilities via scans.                            | Network mapping, Port scanning, Vulnerability scanning                 |
| **Gaining Access**  | Exploiting vulnerabilities to gain unauthorized access.           | SQL injection, Buffer overflow, Phishing                              |
| **Maintaining Access** | Keeping control over the compromised system.                 | Installing rootkits, Hidden users, Tunneling                           |
| **Clearing Tracks** | Erasing traces of the attack to avoid detection.                  | Modifying logs, Deleting evidence of unauthorized access               |



# 🔐 Day 3 - Ethical Hacking: Google Dorking & DNS Reconnaissance

## 📍 Google Dorking

Google Dorking involves using advanced search operators to extract sensitive or hidden information from websites.

### 🔎 Common Google Dorks:

| Operator       | Description                                       | Example Usage                        |
|----------------|---------------------------------------------------|--------------------------------------|
| `site:`        | Restricts results to a specific domain            | `site:example.com`                   |
| `filetype:`    | Searches for specific file types                  | `filetype:pdf site:example.com`      |
| `inurl:`       | Finds URLs containing a specific string           | `inurl:login`                        |
| `intitle:`     | Searches for pages with specific title words      | `intitle:"Google Dorking"`          |
| `allintitle:`  | All specified words in title                      | `allintitle:Google Dorking Tools`   |
| `intext:`      | Search specific text in the body of a webpage     | `intext:"open source intelligence"`  |

---

## 📍 DNS Reconnaissance

DNS Recon is used to gather information about domain infrastructure.

### 🔧 Tools & Commands Used:

#### WHOIS Lookup:
```bash
whois org.com


#** **🧠 Day 4 – Ethical Hacking Journey**

📅 **Date:** 1st August 2025

## 📌 Topics Covered
1. Social Media Reconnaissance  
2. Username Enumeration using Sherlock  
3. Web Technology Fingerprinting  
   - Wappalyzer (Extension)  
   - BuiltWith (Online Tool)  
   - WhatWeb (Command Line Tool)**


---

## 🔍 1. Social Media Reconnaissance
Using LinkedIn and Google Dorks to identify fresh employees or interns in a target organization.

**Google Dork Example:**
```
site:linkedin.com/in/ "org.com"
```

---

## 🕵️‍♂️ 2. Sherlock – Username Enumerator

### 🔹 Quick Install (Kali Linux)
```bash
sherlock
# If not found:
sudo apt install sherlock
```

### 🔸 Manual Install
```bash
git clone https://github.com/sherlock-project/sherlock.git
cd sherlock
pip3 install -r requirements.txt
```

### ▶️ Usage
```bash
sherlock employee_name
```

---

## 🌐 3. Web Technology Fingerprinting

### ✅ Wappalyzer
- Browser Extension
- View CMS, JS libs, and servers used by target site

### ✅ BuiltWith
- Visit https://builtwith.com
- Enter org.com to get full stack report

### ✅ WhatWeb (CLI Tool)
```bash
sudo apt install whatweb
whatweb org.com
```

---

## ✅ Summary Table

| Tool        | Purpose                           | Platform     | Command / URL                    |
|-------------|-----------------------------------|--------------|----------------------------------|
| Sherlock    | Username enumeration              | CLI (Kali)   | sherlock employee_name           |
| Wappalyzer  | Tech stack detection              | Extension    | Browser > Wappalyzer             |
| BuiltWith   | Web tech profiling                | Online tool  | https://builtwith.com            |
| WhatWeb     | Web server + CMS detection        | CLI (Kali)   | whatweb org.com                  |

---

## 📝 Final Notes
- Use OSINT responsibly.
- Combine personal data with web tech info for ethical recon and testing.

