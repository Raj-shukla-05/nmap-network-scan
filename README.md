# 🔍 Day 1: Nmap Local Network Scan

## 📌 Objective
To scan a local network using Nmap to identify live devices and open ports, and to understand the basics of network exposure and security risks.

---

## 🧰 Tools Used
- **Nmap** – for network scanning
- *(Optional)* **Wireshark** – for packet analysis

---

## 🧭 Steps Performed

### ✅ 1. Install Nmap
Downloaded and installed from: [https://nmap.org/download.html](https://nmap.org/download.html)

### ✅ 2. Identify Local Network Range
Used the `ipconfig` (or `ifconfig`) command to find:
- **IP Address**: something like `192.168.X.X`
- **Subnet**: typically `/24`
- So the scan range was: `192.168.X.0/24`

### ✅ 3. Run the Scan
1. ```bash
   nmap -sS 192.168.X.0/24 -oN scan_results.txt
2. -sS: TCP SYN scan
3. -oN: Save results to a text file

### ✅ 4. Analyze the Results
Found 4 live devices

Detected open ports like 80, 443, 135, 445, etc.

Identified services such as HTTP, HTTPS, RPC, and file sharing

### ✅ 5. Save the Results
All scan output saved in: scan_results.txt

🔐 Security Observations
One device had many open web and media ports — may require review

My machine had Windows file-sharing ports open — firewall recommended

Other devices had closed ports — good security posture

📁 Files in This Repo
scan_results.txt — Nmap scan results (MACs and names removed)

README.md — This documentation

✅ What I Learned
How to find my IP range

How to use Nmap to scan a local network

How to identify open ports and related services

How to upload work to GitHub safely

🚀 Next Steps
Learn how to close unnecessary ports or services

Explore deeper scans with nmap -sV

Use Wireshark to analyze packet-level data

