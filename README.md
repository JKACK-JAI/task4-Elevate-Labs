
 # Cybersecurity Internship – Task 4

--Firewall Configuration using UFW on Linux--


#  Objective:
To configure and test basic firewall rules using the ufw (Uncomplicated Firewall) tool in Linux, demonstrating how firewall rules filter network traffic and enhance system security.

#  Tool Used:
✔️ UFW (Uncomplicated Firewall)
UFW is a frontend for iptables designed to simplify the process of configuring a host-based firewall. It enables users to manage firewall rules through simple commands.

 Experiment Overview:
# Step 1: Enabled the Firewall
To start managing incoming and outgoing network traffic, the firewall was activated using:


**sudo ufw enable**

 This ensures UFW starts filtering packets based on rules.

#  Step 2: Blocked Port 23 (Telnet)
Telnet is an outdated protocol that sends data in plaintext. To improve security, we blocked port 23 using:


**sudo ufw deny 23**

 This prevents remote connections over Telnet to the system.

# Step 3: Tested the Firewall Rule
To verify that port 23 was effectively blocked, we used:

**telnet localhost 23**

 Result: Connection was refused or timed out — confirming the firewall rule was active.

# Step 4: Allowed Port 22 (SSH)
To allow secure remote access via SSH, we added an allow rule:


**sudo ufw allow 22**

 This ensures that administrators can still access the system remotely without being blocked.

# Step 5: Verified Active Firewall Rules
All active rules were listed with:

**sudo ufw status numbered**

 Displayed all currently applied firewall rules with numbering for management.

#  Step 6: Removed the Test Rule (Optional)
To restore the original state of the firewall and remove the test block:

**sudo ufw delete deny 23**

Or reset everything:

**sudo ufw reset**

 Learning Outcome:


# Through this task, I learned:

How to enable and configure UFW for basic firewall tasks

The difference between blocking and allowing ports

How to test blocked ports using tools like telnet

Why blocking unsecured ports (like 23) improves security

How to view, manage, and clean firewall rules

#  Screenshots:
All screenshots of terminal outputs have been added in the /screenshots/ folder:

Firewall enabled

Port 23 blocked

Port 22 allowed

Rule verification

Telnet test results

# Useful Commands Summary:

sudo ufw enable
sudo ufw status numbered
sudo ufw deny 23
sudo ufw allow 22
