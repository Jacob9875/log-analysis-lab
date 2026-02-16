## Issue 1 

**Log Entries:**

line 16

2023-02-17 09:34:50 fdf8:f53b:82e4::53 fdf8:f53b:82e4:0:1652:14ff:fe0b:b71c TCP 22 Deny 0

**Description of log entries:** IPv6 host trying SSH, blocked

**Reason for concern:** Strange because internal IPv6 traffic usually isn’t connecting to itself over SSH

**Potential impact:** If a compromised host is scanning SSH on other internal machines, it could be mapping network

**Possible explanations:** Could indicate misconfiguration or scanning

## issue 2 ##

**Log Entries:**

line 1

2023-02-17 09:33:54 192.168.1.24 216.58.194.206 TCP 443 Allow 752489  

**Description of log entries:** large bytes transfer

**Reason for concern:** very large data transfer

**Potential impact:** could indicate data exfiltration

**Possible explanations:** legitimate service

## issue 3 ##

**Log Entries:**

line 27

2023-02-17 09:35:36 192.168.1.163 13.107.246.57 TCP 443 Allow 73240

**Description of log entries:** large bytes transfer

**Reason for concern:** very large data transfer

**Potential impact:** could indicate data exfiltration

**Possible explanations:**legitimate service


## issue 4 ##

**Log Entries:**

line 51

2023-02-17 09:37:17 192.168.1.150 162.159.134.234 TCP 443 Allow 70136


**Description of log entries:** large bytes transfer

**Reason for concern:** very large data transfer

**Potential impact:** could indicate data exfiltration

**Possible explanations:**legitimate service

## issue 5 ##

**Log Entries:**

line 53

2023-02-17 09:37:27 192.168.1.150 162.159.130.233 TCP 443 Allow 72643 

large bytes transfer

**Description of log entries:** large bytes transfer

**Reason for concern:** very large data transfer

**Potential impact:** could indicate data exfiltration

**Possible explanations:**legitimate service

## issue 6 ##

**Log Entries:**

line 3

2023-02-17 09:33:57 192.168.1.33 116.132.235.228 ICMP 0 Allow 98

**Description of log entries:** Likely ping/traceroute

**Reason for concern:** could be recon.

**Potential impact:** could be malware reconaissance

**Possible explanations:** network diagnostics

## issue 7 ##

**Log Entries:**

line 6

2023-02-17 09:34:09 127.0.0.1 127.0.0.1 TCP 3000 Allow 57289

**Description of log entries:** large bytes transfer

**Reason for concern:** very large data transfer

**Potential impact:** could indicate data exfiltration

**Possible explanations:**legitimate service

## issue 8 ##

**Log Entries:**

lines 65-69

2023-02-17 09:38:24 192.168.1.72 111.221.29.254 TCP 443 Deny 0

2023-02-17 09:38:31 192.168.1.72 111.221.29.254 TCP 443 Deny 0

2023-02-17 09:38:39 192.168.1.72 111.221.29.254 TCP 443 Deny 0

2023-02-17 09:38:46 192.168.1.72 111.221.29.254 TCP 443 Deny 0

2023-02-17 09:38:53 192.168.1.72 111.221.29.254 TCP 443 Deny 0

**Description of log entries:** multiple attempts all denied 

**Reason for concern:** repeated attempts after being blocked

**Potential impact:** attempted data exfiltration

**Possible explanations:** could be a legitimate service trying an update and failing or could be malware

## issue 9 ##

**Log Entries:**

line 41

2023-02-17 09:36:44 192.168.1.80 185.151.204.30 TCP 48127 Deny 48

**Description of log entries:** unusual port and a deny

**Reason for concern:** possible rogue process using uncommon high port

**Potential impact:** could indicate data exfiltration

**Possible explanations:** could be command and control attempt

## issue 10 ##

**Log Entries:**

line 5

2023-02-17 09:34:03 192.168.1.27 45.137.80.15 TCP 41284 Deny 48

**Description of log entries:** unusual port and deny

**Reason for concern:** Outbound connection to non-standard high port

**Potential impact:** Could indicate a compromised host trying to reach a command-and-control server

**Possible explanations:** Malware or network scanning reconaissance

## issue 11 ##

**Log Entries:**

line 31

2023-02-17 09:35:56 172.17.99.132 205.185.216.10 UDP 443 Deny 6340

**Description of log entries:** port 443 usually uses TCP and deny

**Reason for concern:** Using UDP 443 could attempt to bypass standard network monitoring

**Potential impact:** Could be malware trying to communicate externally using UDP to evade detection

**Possible explanations:** Malware

## issue 12 ##

**Log Entries:**

lines 46-49

2023-02-17 09:37:04 192.168.1.229 239.255.255.250 UDP 443 Allow 6273

2023-02-17 09:37:07 192.168.1.229 239.255.255.250 UDP 443 Allow 6273

2023-02-17 09:37:09 192.168.1.229 255.255.255.255 UDP 443 Allow 6273

2023-02-17 09:37:14 192.168.1.229 192.168.1.255 UDP 443 Allow 6273  

**Description of log entries:** multiple attempts at fast interval and large transfers of the same and using UDP over 443

**Reason for concern:** UDP is not normally used for broadcast

**Potential impact:** could be unauthorized access 

**Possible explanations:** could be a malware spreading attempt

## issue 13 ##

**Log Entries:**

line 25

2023-02-17 09:35:30 192.168.1.34 35.186.224.47 ICMP 0 Allow 98

**Description of log entries:** Likely ping/traceroute

**Reason for concern:** unusual destination IP and could be recon.

**Potential impact:** could be reconaissance

**Possible explanations:** network diagnostics

## issue 14 ##

**Log Entries:**

lines 71-73

2023-02-17 09:39:03 192.168.1.19 40.94.31.197 TCP 1433 Allow 37419

2023-02-17 09:39:08 192.168.1.19 40.94.25.38 TCP 1433 Allow 32780

2023-02-17 09:39:11 192.168.1.19 40.94.28.182 TCP 1433 Allow 41935

**Description of log entries:** outbound to Microst SQL

**Reason for concern:** potential rogue process or misconfiguration

**Potential impact:** potential data exfiltration

**Possible explanations:** misconfigured application

## issue 15 ##

**Log Entries:**

line 4

2023-02-17 09:34:01 192.168.1.211 62.128.197.131 UDP 51820 Allow 14

**Description of log entries:** unauthorized VPN

**Reason for concern:** covert tunnel possibility

**Potential impact:**  potential data exfiltration

**Possible explanations:** malware

## issue 16 ## 

**Log Entries:**

line 7 

2023-02-17 09:34:14 192.168.1.49 216.109.119.63 TCP 25 Allow 7421

**Description of log entries:** SMTP relay

**Reason for concern:** Potential rogue process / suspicious port activity

**Potential impact:**  botnet activity / data exfiltration

**Possible explanations:** Malware

