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
```bash
nmap -sS 192.168.X.0/24 -oN scan_results.txt
