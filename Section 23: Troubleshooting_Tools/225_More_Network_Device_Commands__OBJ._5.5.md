## 💡 More Network Device Commands (OBJ. 5.5)
This section details additional essential commands for troubleshooting and managing network devices, primarily focusing on Cisco switches, including commands for MAC address tables, ARP, VLANs, and PoE.

✅ **More Network Device Commands**
- Essential commands for troubleshooting and managing network devices, primarily on Cisco switches.

✅ **`show MAC address table`**
- Purpose: Displays the MAC address table on a switch.
- Function: Maps MAC addresses to the switch ports they are connected to.
- Use: Identify devices on specific ports, troubleshoot connectivity.
- Output Columns: VLAN/BID, MAC Address, Type (e.g., dynamic), Port.

✅ **`show ARP`**
- Purpose: Displays the ARP (Address Resolution Protocol) table.
- Function: Shows the mapping of IP addresses to MAC addresses.
- Use: Verify correct IP-to-MAC mappings, detect ARP cache poisoning/spoofing.
- Output Columns: Protocol, Address (IP), Age, Hardware Address (MAC), Type (e.g., ARPA), Interface.

✅ **`show VLAN`**
- Purpose: Displays VLAN (Virtual Local Area Network) settings on a switch.
- Function: Shows VLAN configurations, including VLAN ID, name, status, and associated ports.
- Use: Verify network segmentation, troubleshoot VLAN connectivity issues.
- Output Columns: VLAN ID, Name, Status (active/inactive), Ports.
- **Exam Tip:** Change default VLAN 1 to a less guessable ID for security.

✅ **`show power`**
- Purpose: Displays and configures Power over Ethernet (PoE) settings.
- Function: Shows power allocated, used, and available per port for PoE devices.
- Use: Manage power distribution, troubleshoot PoE issues (e.g., devices not powering on).
- Output Columns: Interface, Admin (auto/manual), Oper (on/off), Power (watts), Device, Class (PoE class), Max (max power supported).