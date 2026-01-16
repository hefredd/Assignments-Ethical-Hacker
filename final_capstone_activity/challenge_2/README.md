# Challenge 2: Information Disclosure via Directory Indexing
## Objective
Use web server misconfigurations to browse the file system and find hidden sensitive files.

## Vulnerability Profile
Vulnerability: Directory Browsing / Information Disclosure.

Severity: Medium.

Target: 10.5.5.12.

## Execution Steps
Reconnaissance: Ran Nikto to scan for server misconfigurations.

Discovery: Identified that the /config/ and /docs/ directories allowed indexing.

Exploitation: Manually navigated to the directories via a web browser and traversed the folder structure to find the hidden challenge flag.

## Remediation
Disable directory listing by modifying server configuration (e.g., Options -Indexes in Apache).

Ensure every directory contains a default index.html or index.php file to prevent index generation.
