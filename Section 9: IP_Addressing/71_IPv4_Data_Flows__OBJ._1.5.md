## 💡 IPv4 Data Flows (OBJ 1.5)

IPv4 data flows describe how information is transmitted from a source to one or more destinations on an IP network.

✅ **Three Main Types of IPv4 Data Flows**
- **1. Unicast:**
  - **Concept:** One-to-one communication. Data is sent from a single source device to a single destination device.
  - **Mechanism:** The source IP address is the sender, and the destination IP address is a specific receiver.
  - **Analogy:** Sending a letter to a single person's mailing address.
  - **Use Cases:** Web browsing (client to web server), email (client to mail server), file transfers between two specific computers.
  - **Example:** Your computer requesting a webpage from `google.com`.
- **2. Multicast:**
  - **Concept:** One-to-many communication. Data is sent from a single source device to a specific group of multiple destination devices that have expressed interest in receiving that data.
  - **Mechanism:** Uses special Class D IP addresses (224.0.0.0 to 239.255.255.255) as the destination. Devices join a "multicast group" to receive the traffic.
  - **Analogy:** Sending a message to a group chat; only members of the group receive it.
  - **Use Cases:** Video conferencing, streaming live events, online gaming, IP television (IPTV), stock tickers.
  - **Benefit:** Efficiently delivers data to multiple interested parties without flooding the entire network (like broadcast) or sending multiple unicast streams.
- **3. Broadcast:**
  - **Concept:** One-to-all communication. Data is sent from a single source device to all other devices within the same network segment (broadcast domain).
  - **Mechanism:** The destination IP address is the broadcast address for that network segment (e.g., `192.168.1.255` for a `192.168.1.0/24` network).
  - **Analogy:** Shouting a message in a room; everyone in that room hears it.
  - **Use Cases:** ARP (Address Resolution Protocol) requests, DHCP (Dynamic Host Configuration Protocol) discovery messages.
  - **Limitation:** Can consume significant network bandwidth and CPU resources on all devices in the broadcast domain, leading to "broadcast storms" if not properly managed (e.g., by routers/VLANs).