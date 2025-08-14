## 💡 Understanding the OSI Model (OBJ 1.1)

Wireshark is a packet analyzer used to pull apart network traffic and understand the OSI model layers. While Wireshark usage is not on the Network+ exam, it's important to know that it's a packet analyzer for troubleshooting.

✅ **Wireshark and OSI Layers**
- **Layer 2 (Data Link):** Shows frames, MAC addresses (source/destination), and encapsulation type (e.g., Ethernet).
- **Layer 3 (Network):** Shows Source and Destination IP addresses.
- **Layer 4 (Transport):** Shows whether TCP or UDP was used.
- **Layer 7 (Application):** Shows application-level protocols like HTTP, FTP, and Telnet, revealing data like HTTP GET requests, FTP transfers, or Telnet session commands.

✅ **Network Analysis**
- Network technicians focus on source, destination, protocol, and ports when analyzing traffic.
- Wireshark captures network traffic into PCAP (packet capture) files.
- Wireshark can be used for security analysis, revealing sensitive information like clear-text usernames and passwords in protocols like Telnet.