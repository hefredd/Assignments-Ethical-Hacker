# Ethical Hacking & Penetration Testing Labs.

## Hands-On Laboratory Research & Vulnerability Analysis.
This repository is a collection of cybersecurity labs focused on Penetration Testing, Vulnerability Management, and Web Application Security. Each lab follows a structured methodology: Reconnaissance, Exploitation, Analysis, and Remediation.

## Repository Structure.
The projects are organized into specialized domains of security testing:

### 1. Web Application Security (Injection Attacks).
Lab: SQL Injection (SQLi) on DVWA.

Tools: DVWA, MySQL, CrackStation.

Key Skills: UNION-based exploitation, database schema enumeration, MD5 hash cracking.

Objective: Bypassing authentication and exfiltrating administrative credentials from a backend database.

### 2. Vulnerability Management.
Lab: Automated Scanning with OWASP ZAP.

Tools: OWASP ZAP, OWASP WSTG.

Key Skills: DAST (Dynamic Application Security Testing), Spidering, RCE analysis (CVE-2012-1823).

Objective: Identifying high-risk server-side vulnerabilities and mapping them to the industry-standard Web Security Testing Guide (WSTG).

### 3. Social Engineering.
Lab: Website Cloning & Credential Harvesting.

Tools: Social Engineering Toolkit (SET).

Key Skills: Site spoofing, POST-back configuration, social engineering vectors.

Objective: Simulating a phishing attack to demonstrate how attackers steal user credentials through cloned login portals.

### 4. Infrastructure & SMB Security.
Lab: SMB Enumeration & File Transfer.

Tools: Nmap, Enum4linux, SMBClient.

Key Skills: Null session testing, share enumeration, data exfiltration.

Objective: Identifying misconfigured SMB shares and demonstrating unauthorized access to internal network files.

## Technical Stack & Tools
Operating System: Kali Linux.
Scanning: Nmap, OWASP ZAP, Enum4linuxExploitationSET (Social Engineering Toolkit), SQL Injection.
Analysis: OWASP WSTG, CrackStation.

## Professional Methodology.
Each lab report within this repository includes:

  #### 1. Executive Summary: High-level overview of the risks.

  #### 2. Technical Steps: Detailed commands and walkthroughs.

  #### 3. Proof of Concept: Screenshots of successful exploitation.

  #### 4. Remediation: Actionable defensive strategies to patch the vulnerabilities.

## Ethical Disclosure.
All activities documented in this repository were conducted within an authorized, isolated, and legal lab environment. The information provided is for educational purposes only. Unauthorized access to computer systems is illegal and strictly prohibited.
