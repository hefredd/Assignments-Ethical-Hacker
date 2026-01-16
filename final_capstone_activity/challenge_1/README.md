# Challenge 1: SQL Injection & Credential Cracking
## Objective: Identify a vulnerable web input to extract database credentials and gain unauthorized access to a secondary server.

## Vulnerability Profile
Vulnerability: Union-Based SQL Injection.

Severity: Critical.

Target: 10.5.5.12 (DVWA).

## Execution Steps
Reconnaissance: Tested input fields with ' to trigger database syntax errors.

Exploitation: Used a UNION SELECT payload to bypass the intended query and dump the users table.

Credential Cracking: Extracted MD5 hashes and used CrackStation to recover the plaintext password for user smithy.

Post-Exploitation: Used the cracked credentials to log into the target at 192.168.0.10 and retrieve the challenge code.

## Remediation
Use Prepared Statements (Parameterized Queries) to prevent input from being interpreted as code.

Enforce the Principle of Least Privilege for database service accounts.
