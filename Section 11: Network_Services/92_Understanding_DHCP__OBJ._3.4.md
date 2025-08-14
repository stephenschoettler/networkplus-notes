## 💡 Understanding DHCP (OBJ 3.4)

- This lesson demonstrates the DHCP process and configuration using a simulated network.
- In a typical SOHO (Small Office/Home Office) setup, the wireless router often acts as the DHCP server.
- All four steps of the DORA process typically involve broadcast messages on the local network segment.

✅ **The DORA Process in Action**
- **D**iscover: Client broadcasts a message to find a DHCP server.
- **O**ffer: DHCP server offers an available IP address from its scope.
- **R**equest: Client requests to use the offered IP address.
- **A**cknowledge: DHCP server sends a final **broadcast acknowledgment**, confirming the IP assignment and lease details to the client.

✅ **DHCP Scope Configuration**
- The DHCP server is configured with a **scope**, which defines the range of IP addresses it can assign.
- Example: A scope might start at 192.168.0.100 and allow for 50 users, meaning IPs from 192.168.0.100 to 192.168.0.149 are assignable.
- The router's own IP address (e.6., 192.168.0.1) typically serves as the default gateway for clients.

✅ **DHCP Reservations**
- **Purpose:** To ensure a specific device always receives the same IP address from the DHCP server.
- **How it works:** The DHCP server is configured with the device's **MAC address** and the desired IP address. When that specific MAC address requests an IP, the server always assigns the reserved IP.
- **Use Cases:** Ideal for devices that need a consistent IP but benefit from DHCP's automated management (e.g., network printers, file servers, specific workstations).
- **Configuration:** Reservations can be added or removed from the DHCP server's settings.