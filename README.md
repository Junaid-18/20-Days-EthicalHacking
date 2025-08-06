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




# 🧠 Day 4 – Social Media Recon and web Finger Printing

## 📌 Topics Covered
1. Social Media Reconnaissance
2. Username Enumeration using Sherlock
3. Web Technology Fingerprinting
   - Wappalyzer (Extension)
   - BuiltWith (Online Tool)
   - WhatWeb (Command Line Tool)

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


# 🛡️ Day 5 – Subdomain Enumeration and Firewalls Identifiers

## 📚 Topics Covered

### 🔹 Subdomain Enumeration

- **What is a Subdomain?**  
  A subdomain is a division of a main domain, used to organize or host specific services like `mail.example.com` or `blog.example.com`.

- **Definition of Subdomain Enumeration**  
  Subdomain enumeration is the process of identifying valid subdomains associated with a target domain. It is a crucial part of reconnaissance in ethical hacking as it uncovers potential entry points that are not visible on the main site.

- **Tools Used:**
  - **Subfinder**  
    Command:  
    ```bash
    subfinder -d org.com
    ```
  - **Online Tool**  
    Visit: [https://subdomainfinder.c99.nl](https://subdomainfinder.c99.nl)

---

### 🔹 Identifying Firewalls

- **What is a Firewall?**  
  A firewall is a network security system that monitors and filters traffic to and from a network. It helps protect against unauthorized access.

- **Tool Used:**
  - **wafw00f**  
    Command:  
    ```bash
    wafw00f https://org.com
    ```
    If it doesn't work, try:
    ```bash
    sudo wafw00f https://org.com
    ```
  🔎 Note: This tool may successfully detect firewalls for some domains but might fail for others depending on the WAF configuration.

---

## 📝 Observations

- Subdomain enumeration tools like Subfinder and online lookup services are effective in identifying exposed infrastructure.
- Firewall detection is sometimes limited by server-side settings and protection mechanisms.
- These tools are essential in the **Reconnaissance** phase of ethical hacking.

---

📄 **[Download the Day 5 Detailed Report](./Day5.docx)**  
📁 Folder: `Day5/`  


# 🧠 Day 6 – Active Reconnaissance & Nmap Scanning

## 🔍 Topic: Active Reconnaissance
Active reconnaissance involves directly interacting with a target system to gather information. Unlike passive reconnaissance, it's **detectable** and **may trigger alerts** on IDS/IPS systems.

**Examples include:**
- Port Scanning
- OS Detection
- Service Enumeration
- Vulnerability Scanning

**Tools used:** Nmap, Netcat, Hping

---

## 📌 What are Ports?
Ports are virtual communication endpoints used to identify specific processes or network services.

| Port | Service         | Use                        |
|------|------------------|-----------------------------|
| 20   | FTP Data         | File transfer               |
| 21   | FTP Command      | FTP control                 |
| 22   | SSH              | Secure shell (remote login) |
| 25   | SMTP             | Email service               |
| 53   | DNS              | Domain name resolution      |
| 80   | HTTP             | Web (non-secure)            |
| 443  | HTTPS            | Web (secure)                |

---

## 🔗 What are Protocols?
- **TCP** – Connection-oriented, reliable
- **UDP** – Connectionless, faster but unreliable

---

## 🛠️ Nmap Tool Overview

Nmap (Network Mapper) is used for:
- Host discovery
- Port scanning
- OS & version detection
- Running vulnerability scripts

### ✅ Command we used:
```bash
sudo nmap -sS -sV -sC -O scanme.nmap.org
sudo nmap -A org.com
```


# 🛡️ Day 7 – Directory Bruteforcing 

---

## 🔍 What is a Directory?

In web applications, a **directory** is like a folder that stores web pages, configuration files, scripts, and other components. Some directories are hidden or not linked publicly, making them vulnerable if they contain sensitive data such as:
- Admin panels
- Backups
- Configuration files

Directory Bruteforcing helps uncover these hidden folders by trying many possible paths using a **wordlist**.

---

## 🛠️ Practical Steps

### ✅ Step 1: Start the Machine
We used the **"Vulnversity"** machine on [TryHackMe](https://tryhackme.com), copied the **target IP address**, e.g.:

```bash
http://10.10.188.89
🚀 Tool 1: Gobuster (for HTTP)
🔹 Command:
bash
Copy
Edit
gobuster dir -u http://10.10.188.89 -w /usr/share/seclists/Discovery/Web-Content/common.txt
🔹 Explanation:
Flag	Description
dir	Directory brute-force mode
-u	Target URL
-w	Path to the wordlist file

⚠️ If the wordlist path doesn't work, check:

bash
Copy
Edit
ls /usr/share/seclists/Discovery/Web-Content/
Or install Seclists:

bash
Copy
Edit
sudo apt install seclists
📄 Sample Output:
bash
Copy
Edit
/.htaccess (Status: 403)
/.hta       (Status: 403)
/admin      (Status: 301)
/uploads    (Status: 301)
403: Forbidden – file/folder exists but access is denied.

301: Moved Permanently – folder exists and can be accessed.

🔐 Gobuster HTTPS Limitation
Gobuster may fail with HTTPS URLs due to certificate or SSL issues. That’s why we switch to Feroxbuster for HTTPS scanning.

🚀 Tool 2: Feroxbuster (for HTTPS)
🔹 Command:
bash
Copy
Edit
feroxbuster --url https://10.10.188.89 -w /usr/share/seclists/Discovery/Web-Content/common.txt
✅ Why Feroxbuster?
Works well with HTTPS

Supports recursion

Automatically handles redirects

Easy and fast

🔧 Install it:
bash
Copy
Edit
sudo apt install feroxbuster
📂 Wordlist Location in Kali Linux
To find common wordlists:

bash
Copy
Edit
ls /usr/share/seclists/Discovery/Web-Content/
Or search directly:

bash
Copy
Edit
sudo find / -name "common.txt" 2>/dev/null

🧠 Summary
Tool	Protocol	Usage Purpose	Wordlist Path
Gobuster	HTTP	Fast directory bruteforcing	/usr/share/seclists/Discovery/Web-Content/common.txt
Feroxbuster	HTTPS	Secure brute-forcing	/usr/share/seclists/Discovery/Web-Content/common.txt
```

# 🛡️ Day 8 – Vulnerability Scanning with Nessus Essentials

## 🔍 What is Vulnerability Scanning?

Vulnerability scanning is an automated method to identify weaknesses in systems, networks, and applications. These weaknesses may include outdated software, unpatched vulnerabilities, or misconfigurations.

It is a core part of cybersecurity hygiene, allowing organizations to detect risks before they can be exploited.

---

## 🧾 Types of Vulnerability Scans

| **Scan Type**             | **Description**                                                                                   | **Access Level**            | **Purpose**                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------------------------|
| **External Scans**        | Scans externally-facing IPs to find perimeter/cloud vulnerabilities.                              | Public-facing               | Assess external security posture.                                           |
| **Internal Scans**        | Run inside the network to detect internal risks.                                                  | Internal network access     | Identify post-breach risks.                                                 |
| **Unauthenticated Scans** | No login required; uses public info to detect vulnerabilities.                                    | No credentials required     | Reveal visible weaknesses to outsiders.                                     |
| **Authenticated Scans**   | Uses valid login credentials to deeply assess the system.                                         | Valid user credentials      | Reveal hidden vulnerabilities and compliance issues.                        |

---

## 🛠 Tool Used: Nessus Essentials

[Nessus Essentials](https://www.tenable.com/products/nessus/nessus-essentials) is a free, professional vulnerability scanner by Tenable. It supports scanning up to 16 IP addresses and provides detailed vulnerability insights.

---

## ⚙️ Installation Steps (on Kali Linux)

1. **Download Nessus Essentials**  
   - Get the `.deb` file from the Tenable website.

2. **Navigate to Downloads Directory**  
   bash
   cd Downloads  
   ls
Install Nessus


sudo dpkg -i Nessus-10.x.x-debian6_amd64.deb
Start Nessus Service


sudo systemctl start nessusd.service
Open in Browser


Visit: https://localhost:8834

Click Advanced → Continue to localhost

Register & Setup

Choose Nessus Essentials, register, and receive activation code

Create user credentials and let plugins download
 ```
## 🧪 Practical Task Performed
Launched Nessus dashboard

Created a Basic Network Scan

Entered a target IP and ran the scan

Observed categorized vulnerabilities:

Critical, High, Medium, etc.

Each with CVEs, severity levels, and remediation tips
 ```

✅ Outcome
Understood different types of vulnerability scans

Installed Nessus and set up scanning environment

Executed a real scan and reviewed vulnerability reports

Gained hands-on experience in security auditing



# 🛡️ Day 9 –  Finding Exploits

---

## 📌 Overview

After performing **port scanning** and **service detection** using tools like `nmap`, the next step in penetration testing is **identifying known vulnerabilities or exploits** for the services and software versions running on a target system. This process is often called **exploit enumeration**.

The goal is to map the discovered service/version to a known CVE (Common Vulnerabilities and Exposures) and find a corresponding **public exploit** to further investigate or weaponize.

---

## 🔧 Tools Used

| Tool         | Purpose                                                                 |
|--------------|-------------------------------------------------------------------------|
| `nmap`       | Port scanning and service version detection                             |
| Exploit-DB   | Public exploit database (offline & online)                              |
| Rapid7       | Online vulnerability research and exploit frameworks (e.g., Metasploit) |
| GitHub       | Open-source exploits and POCs                                            |
| `searchsploit` | Offline tool to search for public exploits locally                     |
| `mousepad`   | To view exploit code files                                               |

---

## 🔍 Step-by-Step Process

### ✅ 1. Scan the Target with Nmap

```bash
nmap -sS -sV <target-ip>
```

- `-sS`: SYN scan (stealthy TCP scan)
- `-sV`: Service version detection

**Example Output Snippet:**

```
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
80/tcp   open  http    Apache httpd 2.4.18 ((Ubuntu))
```

---

### ✅ 2. Search for Exploits Manually (Online)

#### 🔹 A. Exploit-DB

- Website: [https://www.exploit-db.com](https://www.exploit-db.com)
- Purpose: Official and community-contributed public exploits and CVEs.
- Search for:
  ```
  Apache 2.4.18 exploit
  ```

#### 🔹 B. Rapid7 / Metasploit Framework

- Website: [https://www.rapid7.com/db/](https://www.rapid7.com/db/)
- Try keywords like:
  ```
  Apache 2.4.18
  OpenSSH 7.2p2
  ```

#### 🔹 C. GitHub

- Use:
  ```
  site:github.com "Apache 2.4.18 exploit"
  ```

---

### ✅ 3. Use Searchsploit (Offline)

```bash
searchsploit Apache 2.4.18
```

**Example Output:**
```
Apache HTTP Server 2.4.18 - mod_http2 DoS | linux/dos/40002.txt
Apache 2.4.18 - Remote Code Execution     | linux/remote/12345.py
```

---

### ✅ 4. Download Exploit for Offline Use

```bash
searchsploit -m linux/remote/12345.py
```

---

### ✅ 5. Read or Edit the Exploit Code

```bash
mousepad 12345.py
```

Use `nano`, `vim`, or `gedit` as alternatives.

---

## 📁 Important Concepts

| Concept              | Explanation                                                  |
|----------------------|--------------------------------------------------------------|
| CVE                  | Public identifier for known vulnerabilities                  |
| PoC                  | Proof-of-Concept code that demonstrates exploitability       |
| RCE / LFI / XSS / DoS| Types of attacks: Remote Code Exec, File Inclusion, etc.     |
| Privilege Escalation | Gaining higher system access                                 |
| Public Exploit       | Exploit code available to the public                         |

---

## 📌 Best Practices

- ✅ Always verify that the exploit version matches the target.
- ✅ Analyze PoC code before running it.
- ✅ Prefer trusted sources: Exploit-DB, Rapid7, GitHub.
- ✅ Use sandbox/VM environment for testing.

---

## 🧪 Example: Full Flow

```bash
nmap -sS -sV 10.10.98.129
searchsploit Apache 2.4.18
searchsploit -m linux/remote/12345.py
mousepad 12345.py
```

---

## ✅ Summary Table

| Step              | Tool / Action              | Example Command                            |
|-------------------|----------------------------|---------------------------------------------|
| Scan Target       | `nmap`                     | `nmap -sS -sV 10.10.98.129`                |
| Search Online     | Exploit-DB / GitHub / R7   | Search `"Apache 2.4.18 exploit"`           |
| Search Offline    | `searchsploit`             | `searchsploit Apache 2.4.18`               |
| Copy Exploit File | `searchsploit -m <path>`   | `searchsploit -m linux/remote/12345.py`   |
| View Code         | `mousepad`, `nano`, etc.   | `mousepad 12345.py`                        |

---

## 🧠 Conclusion

After fingerprinting services using Nmap, tools like Searchsploit, Exploit-DB, Rapid7, and GitHub help in mapping services to known vulnerabilities. This helps security professionals and bug bounty hunters to assess risks, exploit responsibly in labs, and patch or report vulnerabilities effectively.

---
