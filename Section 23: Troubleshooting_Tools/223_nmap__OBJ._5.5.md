## 💡 nmap (Network Mapper) (OBJ. 5.5)
This section introduces nmap, a powerful network scanning tool, detailing its features, common commands for host and service discovery, OS detection, and its utility in network troubleshooting and security assessments.

✅ **nmap (Network Mapper)**
- Purpose: Discover hosts and services on a network by sending packets and analyzing responses.
- Features: Host discovery, service detection, OS detection, version detection, port/IP scanning.
- Use Cases: Port/IP scanning, fingerprinting services (software versions), vulnerability detection, network mapping, documenting networks, identifying rogue devices.

✅ **Key nmap Commands**
- `nmap -sn [IP/range]`
  - **Ping Scan (Host Discovery):** Identifies active hosts on a network.
  - `-sn`: Skips port scan, only performs host discovery.
  - Example: `nmap -sn 10.10.10.0/24` (finds all live hosts in the subnet).
- `nmap -sS [IP/range] -p [port]`
  - **SYN Scan (Stealth Scan):** Identifies open ports without completing the TCP handshake.
  - `-sS`: Performs a TCP SYN scan.
  - `-p [port]`: Scans a specific port.
  - Example: `nmap -sS 10.10.10.0/24 -p 80` (finds hosts with open web servers).
- `nmap -sV [IP]`
  - **Service Version Detection:** Attempts to determine the version of services running on open ports.
  - `-sV`: Enables service version detection.
  - Use: Identify vulnerable software versions.
  - Example: `nmap -sV 10.10.10.10`
- `nmap -O [IP]`
  - **Operating System Detection:** Attempts to determine the OS of the target host.
  - `-O`: Enables OS detection.
  - Example: `nmap -O 10.10.10.10`
- **Combining Commands:** Multiple flags can be combined for comprehensive scans.
  - Example: `nmap -sS -sV -O 10.10.10.10-12` (SYN scan, service version, and OS detection for a range of IPs).

✅ **Output Interpretation & Benefits**
- Shows open/closed ports, service names, and versions.
- Helps identify potential vulnerabilities based on software versions.
- Provides OS information.
- Useful for network reconnaissance and security assessments.