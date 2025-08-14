## 💡 Using VPN Connections (OBJ 3.5)

A VPN (Virtual Private Network) is used to connect a client or private network to another private network over a public network (like the internet) securely.

✅ **Purpose**
- Access internal network resources (file shares, scanners, printers) from remote locations (e.g., hotel room).
- Create a secure, encrypted "tunnel" over an insecure public network to protect data.
- Change apparent geographic location to bypass regional restrictions.

✅ **How VPNs Work**
- Establishes an encrypted tunnel between the client and the VPN server.
- All traffic from the client then goes through this tunnel to the VPN server, and from there out to the internet or the target private network.

✅ **Configuring VPN in Windows**
- Accessed via Network & Internet settings -> VPN.
- **Options to consider:**
  - Allow VPN over metered networks (can consume data quickly).
  - Allow VPN while roaming (data limits may apply).
- **Information needed for setup:**
  - VPN provider/server address.
  - VPN type/protocol (e.g., IKEv2, PPTP, L2TP, SSTP, IPSec).
  - Sign-in type (username/password, smart card, one-time password, digital certificate).

✅ **VPN Protocols**
- **IKEv2 (Internet Key Exchange v2):** Often used with IPSec.
- **PPTP (Point-to-Point Tunneling Protocol):** Older, less secure.
- **L2TP (Layer 2 Tunneling Protocol):** Often used with IPSec for security.
- **SSTP (Secure Socket Tunneling Protocol):** Microsoft proprietary, uses SSL/TLS.

✅ **Security**
- VPNs encrypt data in transit, protecting it from eavesdropping on public networks.

✅ **Location Spoofing**
- By connecting to a VPN server in a different country, your apparent IP address and location change, allowing access to region-restricted content.