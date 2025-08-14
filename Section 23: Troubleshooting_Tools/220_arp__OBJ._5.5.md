## 💡 arp (Address Resolution Protocol) (OBJ. 5.5)
This section introduces the `arp` command, a tool for managing the Address Resolution Protocol (ARP) cache, detailing its purpose, common commands for displaying, deleting, and adding entries, and its utility in network troubleshooting.

✅ **arp (Address Resolution Protocol)**
- Purpose: Displays and modifies entries in the ARP cache on a system.
- ARP Cache: Stores IP addresses and their associated MAC (physical) addresses.
- Function: Allows interaction with Layer 2 (MAC) and Layer 3 (IP) address bindings.
- Availability: Windows, Linux, UNIX, OS X (commands are identical).

✅ **`arp` Commands**
- `arp`: Displays help information.
- `arp -a`: **Display ARP Cache.**
  - Shows all current IP-to-MAC mappings.
  - Output includes: IP Address, Physical Address (MAC), Type (dynamic/static).
  - Common entries seen: Default gateway, network broadcast (e.g., `FF-FF-FF-FF-FF-FF`), multicast addresses (e.g., `239.255.255.250` for WS-Discovery), network broadcast IP (`255.255.255.255`).
- `arp -d [IP_address]`: **Delete Specific Entry.**
  - Deletes the IP-to-MAC mapping for the specified IP from the cache.
- `arp -s [IP_address] [MAC_address]`: **Add Static Entry.**
  - Statically assigns an IP-to-MAC mapping.
  - MAC address format uses hyphens (e.g., `01-00-5E-7F-FF-FA`).
  - Use cases: Pre-configuring entries for devices not yet connected, preventing entries from timing out.
  - Note: Dynamic ARP entries typically time out after ~6 hours.
- `arp -d`: **Clear Entire ARP Cache.**
  - Deletes all dynamic and static ARP entries from the cache.