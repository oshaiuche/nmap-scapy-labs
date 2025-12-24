OS-FINGERPRINTING

OS-fingerprinting is to know the particular Operating System / service running on the particular host and to know the available open port.

**command**

sudo nmap -O 10.6.6.23

Explanation

This command enables operating system detection on the target host.
The -O option allows Nmap to analyze network responses and make an educated guess about the operating system.
Root privileges are required to send and receive the necessary probe packets.

Result

Nmap returned an estimated operating system for the target host.

Result Explanation

Identifying the operating system helps narrow down possible vulnerabilities and guides further enumeration and exploitation techniques.

