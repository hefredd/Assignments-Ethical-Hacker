Website Cloning & SMB Enumeration Lab
This repository contains a comprehensive lab report documenting the methodologies for Credential Harvesting via website cloning and SMB Vulnerability Scanning. These exercises were performed in a controlled environment to demonstrate common attack vectors and identify critical security misconfigurations.
1. Website Cloning (Credential Harvesting)
 
Objective: To demonstrate how social engineering toolkits can clone legitimate sites to steal credentials.

Tools & Methods
Tool: Social Engineering Toolkit (SET)
Target: http://dvwa.vm
Technique: Site Cloner + Custom HTML Import
Workflow:
  1.Initialized SET with Attacker IP 10.6.6.1.
  2.Imported a custom index.html designed to redirect victims.
  3.Captured POST data (usernames/passwords) in the SET harvester.

2. SMB Vulnerability Scanning
   
Objective: To enumerate SMB services and identify information leakage or unauthorized share access.

Tools & Commands
Discovery: nmap -sn 172.17.0.0/24

Enumeration:
enum4linux -U (User listing)
enum4linux -P (Password Policy)
enum4linux -S (Share enumeration)

Exploitation/Access:
smbclient -L //172.17.0.2
smbclient //172.17.0.2/tmp (Anonymous access check)

Key Security Takeaways
a. MFA is Non-Negotiable: Credential harvesting is largely negated by robust Multi-Factor Authentication.
b. SMB Hardening: Null sessions and guest access to shares like /tmp provide attackers with an easy foothold for data exfiltration.
c. User Awareness: Technical controls must be paired with user training to identify suspicious URLs and unexpected redirects.

Disclaimer
This project is for educational and ethical security testing purposes only. All attacks were performed on authorized targets within a private, isolated lab environment. Unauthorized access to computer systems is illegal.
