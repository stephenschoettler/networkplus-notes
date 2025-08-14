## 💡 Virtual Private Network (VPN) (OBJ 3.5)

A Virtual Private Network (VPN) extends a private network across a public network (like the internet), enabling users to send/receive data as if directly connected to the private network. Its purpose is to securely connect remote users/offices to a corporate network over an untrusted public network.

✅ **Types of VPNs**
- **1. Site-to-Site VPN:**
  - **Purpose:** Connects two offices/private networks together (e.g., branch office to headquarters).
  - **Alternative to:** Expensive dedicated leased lines.
  - **Mechanism:** VPN tunnel established between routers at each site.
- **2. Client-to-Site VPN:**
  - **Purpose:** Connects a single remote user (laptop, phone) back to a corporate network.
  - **Mechanism:** VPN tunnel established between the client device and a VPN device at the headquarters.
- **3. Clientless VPN:**
  - **Purpose:** Creates a secure remote access VPN tunnel using a web browser, without requiring software/hardware clients.
  - **Mechanism:** Uses SSL (Secure Sockets Layer) or TLS (Transport Layer Security) tunnels (e.g., HTTPS for secure web browsing).
  - **SSL:** Older, less secure.
  - **TLS:** Newer, more secure.
  - **DTLS (Datagram Transport Layer Security):** UDP-based version of TLS, faster for real-time applications (video, VoIP) while maintaining security.

✅ **Tunneling Methods**
- **1. Full Tunnel VPN:**
  - **Mechanism:** Routes and encrypts all traffic (corporate and internet-bound) through the VPN connection back to headquarters.
  - **Pros:** More secure (all traffic is protected).
  - **Cons:** Can slow down internet browsing (traffic takes a longer path), may prevent access to local network resources (e.g., home printer).
  - **Recommendation:** Use over untrusted networks (e.g., hotel Wi-Fi).
- **2. Split Tunnel VPN:**
  - **Mechanism:** Divides traffic; corporate-bound traffic is routed and encrypted over the VPN, while all other traffic (internet-bound) goes directly out the local internet connection.
  - **Pros:** Better performance for internet browsing.
  - **Cons:** Less secure (internet traffic is unencrypted locally), potential for attackers to pivot through the unencrypted tunnel to the corporate network.

✅ **VPN Protocols (Older & Modern)**
- **Older (lack native encryption, often combined with IPSec):**
  - **L2TP (Layer 2 Tunneling Protocol):** Early VPN, lacks native encryption.
  - **L2F (Layer 2 Forwarding):** Cisco-developed, lacks native encryption.
  - **PPTP (Point-to-Point Tunneling Protocol):** Older, lacks native encryption (Windows adds security features).
- **Modern (overwhelmingly used):**
  - **IPSec (IP Security):** Provides authentication and encryption of packets to create secure communication paths. Often combined with L2TP or IKEv2.