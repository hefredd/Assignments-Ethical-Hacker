# FINAL CAPSTONE PROJECT: Lab Series
## Project Overview
This repository contains a collection of four penetration testing challenges focused on different stages of the attack lifecycle, including Web Vulnerabilities, System Misconfigurations, Network File Sharing, and Packet Forensics. Each lab demonstrates the identification, exploitation, and remediation of a specific security flaw.

## Lab Environment
### Platform:
Kali Linux (Attacker)

### Targets:
10.5.5.0/24 and 192.168.0.0/24 networks

### Core Tools:
Nmap, Nikto, Wireshark, SMBClient, CrackStation, and Burp Suite.

## Portfolio of Challenges
### Challenge 1: SQL Injection
Goal: Bypass authentication and extract database records.

Key Skills: SQL injection payloads, MD5 hash cracking, lateral movement.

Summary: Exploited a vulnerable input field in DVWA to dump user credentials and gain access to a secondary secure server.

### Challenge 2: Web Server Misconfiguration
Goal: Discover hidden data through directory traversal.

Key Skills: Web reconnaissance (Nikto), URL manipulation.

Summary: Identified servers allowing "Directory Indexing," which exposed the internal file structure and sensitive documentation folders.

### Challenge 3: SMB Share Exploitation
Goal: Extract confidential files from unsecured network shares.

Key Skills: SMB enumeration, Null Sessions, network file exfiltration.

Summary: Conducted an anonymous login to a network file server (10.5.5.14) to retrieve internal company workfiles from an unsecured print share.

### Challenge 4: Traffic Analysis & Forensics
Goal: Reconstruct an attack or user session from network packets.

Key Skills: Wireshark filtering, HTTP stream analysis, protocol forensics.

Summary: Analyzed a .pcap file to identify unencrypted HTTP traffic, revealing sensitive URLs and internal server directories.

## Global Remediation Strategies
Across these four labs, several critical security themes emerged. To secure an environment against these threats, the following controls should be implemented:

Encryption Everywhere: Replace all clear-text protocols (HTTP, SMBv1, FTP) with encrypted versions (HTTPS, SMBv3, SFTP) to prevent packet sniffing.

Input Sanitization: Use parameterized queries and strict input validation to negate injection-based attacks.

Hardened Configurations: Disable directory indexing and anonymous "Guest" access to all network services.

Least Privilege: Ensure service accounts and network shares are restricted to only the users who absolutely require access.
