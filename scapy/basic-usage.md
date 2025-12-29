Scapy 

Scapy is a Python-based tool used for generating, sending, receiving, and analyzing network packets.
It allows security professionals to interact with network traffic at a low level for testing and analysis.

1.Starting Scapy

**command**
scapy

Explanation

This command launches the Scapy interactive shell.
The shell allows users to write and execute packet-related commands directly.

Result

The Scapy interactive prompt was displayed, indicating that Scapy started successfully.

Result Explanation

A successful launch confirms that Scapy is installed and ready for packet crafting and analysis.

2. Inspecting the IP Layer in Scapy

**command**
ls(IP)

Explanation

This command lists the fields and attributes of the IP protocol layer in Scapy.
It helps understand how IP packets are structured before creating or modifying them.

Result

Scapy displayed the available fields of the IP layer.

Result Explanation

Viewing the IP fields allows precise packet crafting by knowing which parameters can be set or modified.

3. Packet Sniffing with Scapy

**command**
sniff()

Explanation

This command captures network packets in real time using Scapy.
It listens to network traffic on the active interface and collects packets for analysis.

Result

Live network packets were captured and displayed by Scapy.

Result Explanation

Packet sniffing allows observation of network communication and helps understand how data flows across the network.

4. Testing Packet Capture with Ping

**command**
ping google.com

Explanation

This command was used to generate network traffic that could be observed using Scapy packet sniffing.

Result

The command returned a DNS resolution error indicating that the domain name could not be resolved.

Result Explanation

The error occurred because DNS resolution was unavailable in the lab environment.
Despite this, the step demonstrates how external traffic can be generated for packet capture during analysis.
