# Kali Linux Bug Bounty VM

> **Developed by: Adarsh aka 0x0806**  
> **Version:** 1.0.0  
> **Last Updated:** April 2025  
> **License:** MIT

---

## ✨ Introduction

The **Kali Linux Bug Bounty VM** is a customized, optimized, and fully-loaded virtual machine designed specifically for bug bounty hunters, security researchers, red teamers, and ethical hackers. Developed by **Adarsh aka 0x0806**, this VM brings together the most powerful tools and utilities used in modern offensive security engagements, from reconnaissance to exploitation to reporting.

This VM is not just a toolset; it's an entire ecosystem crafted with precision and efficiency in mind. Whether you're scanning for XSS, fuzzing for LFI, hunting for SSRF, or automating recon at scale, this virtual machine is your ultimate weapon.

---

## 📥 Download

You can download the pre-configured **Kali Linux Bug Bounty VM** from the link below:

🔗 [Download Kali Bug Bounty VM (Gofile)](https://gofile.io/d/wg9QxV)

> 💡 *Ensure you verify the hash and integrity after download.*

---

## 🚀 Key Features

- ✅ Pre-installed bug bounty and pentesting tools  
- ✅ Organized directory structure for clean workflow  
- ✅ Optimized bash/zsh environment with custom aliases and functions  
- ✅ Integrated with notification systems (e.g., notify, ntfy.sh)  
- ✅ Custom scripts for automated recon, fuzzing, and reporting  
- ✅ Firejail and AppArmor profiles for tool sandboxing  
- ✅ Tmux + zsh pre-configured for multitasking  
- ✅ Works out-of-the-box on VirtualBox  
- ✅ Offline and air-gapped operational mode  
- ✅ Supports both CLI and GUI tools  

---

## 👤 Username and Password 

👤 **Username**: `bug`  
🔐 **Password**: `BOUNTY`  

---

## 🌐 Primary Use Cases

- ✔ Web Application Security Testing  
- ✔ API Security Testing  
- ✔ Mobile Application Assessment  
- ✔ Network and Infrastructure Recon  
- ✔ CTFs and Red Teaming  
- ✔ Report Automation and PoC Generation  

---

## 🔍 Reconnaissance Suite

| Tool | Function |
|------|----------|
| **amass** | Subdomain enumeration (passive & active) |
| **subfinder** | Fast passive subdomain enumeration |
| **assetfinder** | Discover related assets |
| **dnsx** | DNS probing and resolution |
| **httpx** | Probes URLs, gets status codes, titles, TLS info |
| **gau / waybackurls** | Extract URLs from public archives |
| **hakrawler / katana** | Web crawling and endpoint enumeration |
| **naabu** | Fast port scanner with service detection |
| **shuffledns** | Mass DNS brute-forcing |
| **nmap** | The classic network scanner with NSE support |
| **MassDNS** | High-performance DNS resolver |
| **arjun / paramspider** | Parameter discovery and fuzzing |

---

## 🔮 Vulnerability Scanners

| Tool | Type |
|------|------|
| **nuclei** | Templated vulnerability scanning (CVE, misconfig, etc.) |
| **jaeles** | Modular vulnerability scanner (like nuclei) |
| **dalfox** | DOM and Reflected XSS detection |
| **xsstrike** | Advanced XSS analysis and exploitation |
| **sqlmap** | SQLi automation |
| **ffuf / dirsearch** | Fast fuzzers for directories, APIs, and parameters |
| **kiterunner** | Wordlist-based API discovery |
| **wafw00f** | WAF detection tool |
| **gf patterns** | Grep patterns for hunting parameters (SSRF, XSS, etc.) |

---

## 🔓 Exploitation & Post Exploitation

| Tool | Purpose |
|------|---------|
| **Burp Suite Pro/Community** | Web Proxy for manual testing |
| **Metasploit** | Framework for remote exploits |
| **BeEF** | Browser Exploitation Framework |
| **Responder** | Poisoning LLMNR, NBT-NS |
| **Bettercap** | MITM + WiFi spoofing |
| **CSRF POC Maker** | CSRF payload generation |
| **JWT Tool** | JWT analysis and manipulation |
| **XSS Hunter** | Track out-of-band XSS |
| **OOB POC** | Generate OOB payloads and monitor them |
| **Interactsh Client** | Automated OOB interaction detection |

---

## 📱 Mobile and API Testing

| Tool | Function |
|------|----------|
| **MobSF** | Mobile Security Framework for APK/IPA analysis |
| **Frida / objection** | Dynamic instrumentation and runtime manipulation |
| **Apktool / jadx** | Decompile and analyze APKs |
| **Postman / Insomnia** | Manual API testing |
| **Amass + Swaggerhunter** | Swagger file discovery and endpoint parsing |

---

## 📢 Wordlists & Payloads

- [x] SecLists (Discovery, Fuzzing, Payloads, Passwords)  
- [x] PayloadsAllTheThings (XSS, LFI, SSRF, SSTI, etc.)  
- [x] DNSRecon Lists  
- [x] Fuzzing patterns for parameters and headers  
- [x] Custom Payloads by 0x0806 for bypassing filters and WAFs  

---

## 📚 Reporting Templates

- Markdown-based reporting format (importable to Hacktivity/HTB/BBP)  
- CVSS Score Auto-Calculator  
- PoC + Screenshot + Request/Response format  
- Custom HTML exporter for client-ready reports  

---

## 🪖 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| RAM       | 8 GB    | 16+ GB       |
| CPU       | 2 Cores | 4+ Cores     |
| Disk      | 60 GB   | 100+ GB SSD  |
| Platform  | VirtualBox | Any Hypervisor |

---

## 🔥 Customizations

- Pre-loaded with ZSH + Oh-My-Zsh + Powerlevel10k  
- Tmux + Custom Splits + Logging Enabled  
- Visual Recon Dashboard in CLI  
- Vim + VSCode CLI with custom extensions  
- One-click service startup: Burp, Docker API Labs, Local HTTP server  

---

## 📈 Sample Workflow

```bash
# Recon
subfinder -d target.com -o subs.txt
dnsx -l subs.txt -o resolved.txt
httpx -l resolved.txt -o live.txt

# Vulnerability Scanning
nuclei -l live.txt -t ~/nuclei-templates -o nuclei-results.txt

# Fuzzing
ffuf -u https://site.com/FUZZ -w /opt/wordlists/dir.txt

# XSS Check
dalfox file urls.txt -o xss.txt

# PoC Generation
report_gen.sh target.com
