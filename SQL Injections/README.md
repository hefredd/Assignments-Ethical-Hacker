SQL Injection Exploitation
Overview
This lab demonstrates the process of identifying and exploiting a Union-Based SQL Injection vulnerability within the Damn Vulnerable Web Application (DVWA). The goal was to bypass application logic and extract sensitive information directly from the backend MySQL database.

Learning Objectives
Confirming SQLi vulnerabilities using boolean logic (' OR 1=1 #).

Determining database structure using the ORDER BY and UNION SELECT techniques.

Enumerating database names, versions, and table schemas.

Exfiltrating and cracking administrative password hashes.

Execution Steps
1. Discovery
By injecting ' OR 1=1 #, I forced the database to evaluate the query as TRUE for every row, resulting in a full dump of user IDs and surnames, confirming the input field was unsanitized.

2. Fingerprinting the Database
I used the ORDER BY clause to find the column count:

1' ORDER BY 2 # → Success

1' ORDER BY 3 # → Error (Confirmed 2 columns are in use).

3. Data Exfiltration
Using UNION SELECT, I extracted the following metadata:

DBMS Version: VERSION()

Current Database: DATABASE() (Result: dvwa)

Table Names: Queried information_schema.tables.

Column Names: Queried information_schema.columns for the users table.

4. Credential Cracking
I extracted MD5 password hashes for all users. The admin hash was then processed through CrackStation to retrieve the cleartext password.

Remediation Strategies
To secure the application against these attacks, the following mitigations were researched:

Parameterized Queries: Using prepared statements ensures the database engine treats input as data, not executable code.

Stored Procedures: Similar to parameterized queries, these prevent dynamic string concatenation.

Input Sanitization: Stripping special characters like ', --, and # from user input.
