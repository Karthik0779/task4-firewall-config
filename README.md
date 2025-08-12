

# 🔥 Firewall Configuration Guide (Windows & Linux) 🔥

A simple guide to configuring firewalls on Windows and Linux systems to help secure your network by controlling inbound and outbound traffic.

---

## 📋 Project Overview

This repository contains instructions and commands to configure firewalls on Windows and Linux machines. It covers the built-in Windows Defender Firewall and popular Linux firewall tools such as iptables and firewalld.

---

## ⚙️ Installation & Setup

There’s no installation required for this guide itself, but ensure you have:

- Windows 10/11 or later with administrative rights.
- A Linux distribution with **iptables**, **firewalld**, or **ufw** installed.
- Access to terminal or PowerShell with admin privileges.

---

## 🔧 Firewall Configuration (Windows & Linux)

### 🪟 Windows Firewall Configuration

- **Access:**  
  Open **Windows Defender Firewall** via Control Panel or search in the Start menu.

- **Common tasks:**  
  - ✅ Enable or disable firewall  
  - 🚫 Allow/block apps and features  
  - 🔐 Create inbound/outbound rules

- **Creating a new firewall rule:**  
  1. Open **Windows Defender Firewall with Advanced Security**  
  2. Select **Inbound Rules** or **Outbound Rules**  
  3. Click **New Rule**  
  4. Choose rule type: Program, Port, Predefined, or Custom  
  5. Specify program path or port number  
  6. Select action: **Allow** or **Block**  
  7. Apply to profiles: Domain, Private, Public  
  8. Name the rule and finish

- **PowerShell example to allow HTTP (port 80):**  
  ```powershell
  New-NetFirewallRule -DisplayName "Allow HTTP" -Direction Inbound -Protocol TCP -LocalPort 80 -Action Allow


---

🐧 Linux Firewall Configuration

Common firewall tools include iptables, firewalld (CentOS/RHEL/Fedora), and ufw (Ubuntu/Debian).

Using iptables

View current rules:

sudo iptables -L -v -n

Allow SSH (port 22):

sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT

Drop all incoming traffic by default:

sudo iptables -P INPUT DROP

Save rules:

sudo iptables-save > /etc/iptables/rules.v4


Using firewalld (CentOS/RHEL/Fedora)

Check firewall status:

sudo firewall-cmd --state

Allow port 80/tcp permanently:

sudo firewall-cmd --permanent --add-port=80/tcp
sudo firewall-cmd --reload

List allowed ports and services:

sudo firewall-cmd --list-all



---

🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements, additional examples, or support for other firewall tools.


---

📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

