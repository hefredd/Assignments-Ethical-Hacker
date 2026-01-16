# Challenge 4: Network Traffic Analysis (PCAP)
## Objective 
Analyze a packet capture file to reconstruct user activity and identify clear-text data transmission.

## Vulnerability Profile
Vulnerability: Clear-text Communication (Insecure Protocol).

Severity: Medium.

Tool: Wireshark.

## Execution Steps
Analysis: Opened SA.pcap in Wireshark and applied an http filter.

Identification: Isolated HTTP GET requests to target 10.5.5.11 revealing paths to /passwords/ and /data/.

Retrieval: Reconstructed the URLs from the traffic and used a browser to access the exposed files and retrieve the flag.

## Remediation
Encrypt Traffic: Implement HTTPS (TLS/SSL) to ensure that URLs and data are encrypted during transit.

Secure File Transfer: Use encrypted protocols like SFTP or SCP for moving sensitive data.
