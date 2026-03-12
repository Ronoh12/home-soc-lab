
# Suspicious DNS Traffic Investigation

## Objective
Investigate DNS traffic to identify potentially suspicious domain queries.

## Tools Used

- Wireshark
- PowerShell

## Investigation Scenario

DNS queries were generated using the nslookup command to simulate domain lookups.

Commands used:

nslookup google.com  
nslookup github.com  
nslookup wikipedia.org  

## Detection Method

Network traffic was captured using Wireshark and filtered using:

dns

This filter shows all DNS queries and responses.

## Observations

DNS queries were observed for several domains including:

- google.com
- github.com
- wikipedia.org

Each query requested an A record to resolve the domain name into an IP address.

## Security Significance

DNS traffic analysis can help security teams detect:

- Malware contacting command-and-control servers
- Data exfiltration through DNS
- Suspicious domain activity
- DNS tunneling attacks

Monitoring DNS traffic is an important technique for detecting malicious activity.

## Conclusion

The captured DNS traffic demonstrates how domain queries appear in packet captures and how analysts can investigate DNS activity using Wireshark.