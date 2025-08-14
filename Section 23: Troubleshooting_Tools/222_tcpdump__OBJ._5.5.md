## 💡 tcpdump (OBJ. 5.5)
This section introduces `tcpdump`, a command-line packet analyzer, detailing its purpose, basic usage, filtering capabilities, and its role in network troubleshooting and security analysis.

✅ **tcpdump**
- Purpose: Command-line tool to display TCP/IP and other packets transmitted or received over a network.
- Availability: Default on Linux/Unix/OSX; requires install on Windows.
- Output: Dumps traffic to screen; can save to PCAP files (`.pcap`) for later analysis.

✅ **PCAP Files**
- Packet Capture files (`.pcap`).
- Can be analyzed by `tcpdump` or graphical tools like Wireshark.

✅ **tcpdump Output Format (per packet)**
- Timestamp
- IPv4 (IP) or IPv6 (IP6) notation
- Source IP:Port
- Destination IP:Port
- TCP flags, Sequence number, Acknowledgement number, Windowing number, Packet length.

✅ **Basic Usage**
- Requires `sudo` (administrative permissions) to enable promiscuous mode.
- `sudo tcpdump -i [interface]` (e.g., `en0`, `eth0`) - Captures all traffic on specified interface.

✅ **Filtering Traffic**
- During live capture or when reading from a PCAP file.
- `src [IP_address]` - Filter by source IP.
- `dst [IP_address]` - Filter by destination IP.
- `port [port_number]` - Filter by port (source or destination).
- `src port [port_number]` - Filter by source port.
- `dst port [port_number]` - Filter by destination port.
- Combine filters with `and`, `or`.
- Example: `sudo tcpdump src 10.128.1.130 and src port 5475`

✅ **Saving & Reading PCAP Files**
- Save: `sudo tcpdump -w [filename.pcap] [filters]`
- Read: `sudo tcpdump -r [filename.pcap] [filters]`

✅ **Viewing Packet Contents**
- `-x`: Shows packet contents in both hexadecimal and ASCII.
- Useful for analyzing unencrypted protocols (e.g., FTP, HTTP).

✅ **Filtering Strategy**
- **Filter during collection:** For known specific traffic (reduces file size).
- **Collect everything, then filter:** If indicators of compromise are unknown (requires more storage).

✅ **Relationship with Wireshark**
- `tcpdump` is command-line; Wireshark is graphical.
- PCAP files from `tcpdump` can be opened in Wireshark for advanced analysis.