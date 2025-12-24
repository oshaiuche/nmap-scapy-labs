 NMAP BASIC SCAN

This section documents basic Nmap commands used to verify installation and perform initial network discovery.

 1. Nmap Version Check

**Command**

nmap -v

Explanation

This command displays the Nmap version and confirms that Nmap is properly installed.

Result

Nmap version information was displayed successfully.

2. Network interface check
   
**command**

ip a

Explanation

Displays network interfaces and IP addresses assigned to the system.

Result

The system IP address and active network interface were identified.

3. Host Discovery
   
   **command**
   
   -sn 10.6.6.1/24
   
   -sn → Performs host discovery only (no port scanning)
   
   10.6.6.1/24 → Target IP address
   
This command checks if the target system is online without scanning its ports.

Result

The scan returned a response from the target host, indicating that the system is up and reachable.

Result Explanation

A successful response means the host is active and can be scanned further.
If no response was received, the host could be offline or blocking probe packets.

