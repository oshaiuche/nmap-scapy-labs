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

![Scapy Launch](/screenshots/scapy-launch.png)

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

![Fields of IP](/screenshots/ls-ip.png)

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

![Packet Sniff](/screenshots/sniff-ping.png)

4. Generating Traffic with Ping

**command**
ping www.google.com

Explanation

This command was used to generate network traffic that could be captured and analyzed using Scapy packet sniffing.

Result

The ping command successfully sent and received ICMP packets from www.google.com.

Result Explanation

The successful ping confirms network connectivity and DNS resolution.
The generated ICMP traffic could be observed and analyzed using Scapy during packet capture.

5. Storing Captured Packets

**command**
Paro = _

Explanation

This command captures network packets and stores them in the variable paro.
Instead of only displaying packets, Scapy saves them so they can be analyzed later.

Result

Network packets were successfully captured and stored in the paro variable.

Result Explanation

Storing packets in a variable allows further inspection, filtering, or analysis of the captured traffic within Scapy.

6. Sniffing on a Specific Interface

**command**
sniff(iface="br-internal")

Explanation

This command captures network packets from a specific network interface.
The iface parameter tells Scapy which interface to listen on.

Result

Scapy captured packets from the br-internal interface.

Result Explanation

Selecting a specific interface ensures that only traffic from the intended network segment is captured for analysis.

