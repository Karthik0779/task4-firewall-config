# Task 4 – Firewall Configuration (Windows & Linux)

This task was part of my Cybersecurity Internship. I learned how to configure firewall rules on both **Windows** and **Kali Linux** systems to allow or block network traffic.

---

## 🔧 Tools Used
- Windows Defender Firewall (GUI)
- UFW on Kali Linux (Command Line)
- Telnet (for testing blocked ports)

---

## 💡 What I Did

### 🔷 Windows:
- Opened firewall settings using `wf.msc`
- Blocked port **23** (Telnet)
- Tested using `telnet localhost 23` → connection failed ✅
- Allowed port **22** (SSH)
- Deleted the Telnet rule after testing

### 🐧 Linux (Kali with UFW):
- Installed and enabled UFW
- Blocked port **23** (Telnet)
- Tested using `telnet localhost 23` → connection refused ✅
- Allowed port **22** (SSH)
- Deleted the Telnet rule

---

## 📘 What I Learned
- How to manage firewall rules on Windows and Linux
- How to block insecure ports like Telnet (port 23)
- Importance of allowing secure services like SSH (port 22)
- How to test firewall behavior using Telnet

---

## 📁 Files Included

- `docs/` folder:
  - Linux and Windows firewall reports
  - Commands used
  - Learning summary

- `screenshots/` folder:
  - Step-by-step screenshots for both systems

---

## ✅ Result
Successfully configured, tested, and managed firewall rules on both Windows and Kali Linux.

