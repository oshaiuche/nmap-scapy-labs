PORT-SCANNING

Port scanning in Nmap is the process of using the Nmap tool to send specially crafted packets (probes) to a target computer's network ports (like TCP/UDP 1-65535) to discover which ones are open, closed, or filtered, revealing running services, potential vulnerabilities, and security measures like firewalls, crucial for network security audits and penetration testing. 

**command**

nmap -p 21 -sV -A -T24 10.6.6.23

Explanation

This command performs a targeted scan on port 21 with advanced detection enabled.
It identifies the service running on the port, attempts OS detection, and runs default Nmap scripts to gather additional information.

Command Breakdown

-p 21 → Scans only port 21

-sV → Detects service version

-A →  Aggressive scanning, enables OS detection, script scanning, and traceroute

-T4 → Adjusts scan timing for faster execution

10.6.6.23 → Target IP address

Result

The scan detected the service running on port 21 and provided additional system and service information.

Result Explanation

Service and version detection helps identify outdated or vulnerable services.
The additional data gathered supports deeper security analysis and risk assessment.
