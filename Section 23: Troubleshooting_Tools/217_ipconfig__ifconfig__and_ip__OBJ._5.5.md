## 💡 ipconfig, ifconfig, and ip (OBJ. 5.5)
This section introduces `ipconfig`, `ifconfig`, and `ip` commands, essential tools for displaying and configuring network interface parameters across different operating systems.

✅ **ipconfig, ifconfig, and ip**
- Command-line tools for displaying and configuring network interface parameters.

✅ **`ipconfig` (Windows)**
- Purpose: Displays TCP/IP configuration, refreshes DHCP/DNS.
- `ipconfig`: Basic info (IP, Subnet, Gateway).
  - APIPA (169.254.x.x) indicates DHCP issue.
- `ipconfig /release`: Releases current IP.
- `ipconfig /renew`: Obtains new IP from DHCP.
- `ipconfig /all`: Displays full details (MAC, DHCP/DNS servers, lease times).

✅ **`ifconfig` (Linux/Unix/OS X - Deprecated)**
- Purpose: Displays and configures network interfaces.
- `ifconfig [interface]`: Info for specific interface (e.g., `ifconfig eth0`).
- `ifconfig -a`: Shows all interfaces (active/inactive).
- `ifconfig [interface] up/down`: Activates/disables interface.
- Note: Deprecated; `ip` is the modern replacement.

✅ **`ip` (Linux/Unix/OS X - Modern Replacement for `ifconfig`)**
- Purpose: Comprehensive tool for network configuration.
- `ip a` (or `ip address`): Displays interface configuration.
- `ip a add [IP/CIDR] dev [interface]`: Assigns static IP.
- `ip a del [IP/CIDR] dev [interface]`: Removes IP.
- `ip link set dev [interface] address [MAC]`: Changes MAC address.
- `ip link set dev [interface] promisc on`: Enables promiscuous mode.
- `ip link set dev [interface] up/down`: Activates/disables interface.