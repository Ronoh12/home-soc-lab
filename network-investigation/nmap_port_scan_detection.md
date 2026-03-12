# Port Scan Detection Investigation

## Objective
Detect network reconnaissance activity using packet capture analysis.

## Tools Used

- Nmap
- Wireshark
- PowerShell

## Attack Simulation

A TCP SYN port scan was executed using Nmap against the local host.

Command used:

nmap -sS localhost

This scan sends SYN packets to multiple ports to identify open services.

## Detection Method

Network traffic was captured using Wireshark.

Filter used:

tcp.flags.syn == 1 and tcp.flags.ack == 0

This filter displays SYN packets used during scanning activity.

## Observations

Multiple SYN packets were sent to different destination ports.

This pattern is consistent with reconnaissance behavior.

## Security Significance

Port scanning is commonly used by attackers to:

- Identify open services
- Discover vulnerable systems
- Map network infrastructure

Early detection helps security teams respond before exploitation occurs.

## Conclusion

The captured traffic demonstrates how reconnaissance activity appears in packet captures and how SOC analysts can detect scanning patterns.