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

2. Service Enumeration on SMB Ports

  Service Enumeration on SMB (Server Message Block) ports, primarily TCP 139 and TCP 445, is the process of gathering information 
  about shared resources, users, and potential vulnerabilities on a target system.

  **command**

  nmap -A -p139,445 10.6.6.23

  Explanation

  This command performs an advanced scan on SMB-related ports.
  It detects running services, attempts OS identification, and runs default Nmap scripts to gather additional information from the 
  target.

  Command Breakdown

  -A → [Aggressive scanning] Enables OS detection, script scanning, and traceroute

  -p 139,445 → Targets SMB ports (NetBIOS and SMB)

  10.6.6.23 → Target IP address

Result

The scan returned information about the services running on ports 139 and 445.

Result Explanation

SMB services can reveal valuable system and network information.
Enumerating these ports helps identify potential misconfigurations or security weaknesses.

3. SMB Share Enumeration

**command**
nmap --script smb-enum-shares.nse -p 445 10.6.6.23

Explanation

This command uses an Nmap NSE script to enumerate shared resources on the target system.
It queries the SMB service to identify available network shares and their access permissions.

Command Breakdown

--script smb-enum-shares.nse → Runs the SMB share enumeration script

-p 445 → Targets the SMB service port

10.6.6.23 → Target IP address

Result

The scan returned a list of SMB shares available on the target system.

Result Explanation

Enumerated shares may expose sensitive files or allow unauthorized access.
This information is useful for assessing potential lateral movement or data exposure.
