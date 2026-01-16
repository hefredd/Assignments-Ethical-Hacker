# Challenge 3: Unsecured SMB Share Access
## Objective
Discover and exploit unsecured network shares to exfiltrate confidential files.

## Vulnerability Profile
Vulnerability: Anonymous SMB Access (Null Sessions).

Severity: High.

Target: 10.5.5.14.

## Execution Steps
Reconnaissance: Scanned the 10.5.5.0/24 subnet using Nmap to find open ports 139/445.

Enumeration: Used smbclient -L to list available shares. Discovered that workfiles and print$ allowed anonymous logins.

Exploitation: Connected to the print$ share using a Null Session and used the get command to download the challenge code file.

## Remediation
Disable Guest Access: Configure SMB to require authentication for all shares.

Restrict Null Sessions: Modify registry/configuration settings to prevent anonymous enumeration of shares.
