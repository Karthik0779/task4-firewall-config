Configure and test basic firewall rules to allow or block traffic on specific ports.
🖥 Option 1: Windows Firewall
1️⃣ Open Firewall Settings
Press Windows + R
Type: control firewall.cpl
Press Enter.
2️⃣ View Current Rules
Click Advanced settings on the left panel.
This opens Windows Defender Firewall with Advanced Security.
In the left panel, click Inbound Rules to view existing rules.
3️⃣ Block Inbound Traffic on Port 23 (Telnet)
In Inbound Rules, click New Rule (on right panel).
Select Port → TCP → Specific local ports: 23 → Block the connection.
Choose all profiles (Domain, Private, Public).
Name it Block Telnet Port 23.
4️⃣ Test the Rule
Open Command Prompt.
Run: telnet localhost 23 (If Telnet client isn’t installed, you can enable it via “Turn Windows features on or off.”)
It should fail to connect.
5️⃣ Remove the Test Rule
Go back to Inbound Rules.
Right-click the Block Telnet Port 23 rule and Delete.
🖥 Option 2: Linux (UFW – Uncomplicated Firewall)
1️⃣ Check Firewall Status
sudo ufw status

2️⃣ Enable UFW (if disabled)
sudo ufw enable

3️⃣ Block Port 23 (Telnet)
sudo ufw deny 23/tcp

4️⃣ Allow SSH (Port 22)
sudo ufw allow 22/tcp

5️⃣ Check Rules
sudo ufw status numbered

6️⃣ Test the Rule
Try: telnet localhost 23
It should fail to connect.
7️⃣ Remove the Rule
sudo ufw delete deny 23/tcp

The outcome of this
View and interpret current firewall rules.
Add inbound and outbound rules to allow or block specific ports/services.
Test firewall behavior to confirm it is blocking or allowing traffic as intended.
Safely remove or revert rules to restore the system’s original state.
Understand how a firewall acts as a security barrier between your device and potential threats.
In short — by completing this task, you’ll know how to configure, test, and manage firewall rules on both Windows and Linux.
