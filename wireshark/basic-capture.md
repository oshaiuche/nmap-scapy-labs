Wireshark Definition

Wireshark is a network tool used to capture, monitor, and analyze network traffic by inspecting individual data packets transmitted over a network.

1. Network Interface Identification

**command**
ifconfig

Explanation

This command displays the available network interfaces on the system along with their IP addresses and status.
It is used to identify the active interface to capture traffic from in Wireshark.

Result

The system listed the available network interfaces and their network configuration.

Result Explanation

Identifying the correct network interface ensures that Wireshark captures traffic from the intended network segment.

![ifconfig](/screenshots/ifconfig.png)

2. Default Gateway Identification

**command**
ip route

Explanation

This command displays the system’s routing table.
It is used to identify the default gateway and confirm which network interface is being used to send traffic.

Result

The routing table showed the default route and indicated that traffic is routed through the eth0 interface.

Result Explanation

The default route confirms that eth0 is the primary interface for network communication, making it the correct interface to use for packet capture in Wireshark.

![ip route](/screenshots/wireshark-iproute.png)

3. Packet Capture Using Tcpdump

**command**
sudo tcpdump -i eth0 -s 0 -w dre.pcap

Explanation

This command captures network traffic on the eth0 interface and saves it to a file.
The captured packets are written to a .pcap file, which can later be opened and analyzed in Wireshark.

Command Breakdown

sudo → Required for packet capture

-i eth0 → Specifies the network interface

-s 0 → Captures full packet data

-w dre.pcap → Writes captured traffic to a file

Result

Network packets were successfully captured and saved to the dre.pcap file.

Result Explanation

Saving traffic to a capture file allows offline analysis in Wireshark without needing to capture live traffic again.

![Captured Network Traffic](/screenshots/capture.png)
