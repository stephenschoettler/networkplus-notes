## 💡 Generic Routing Encapsulation (GRE) (OBJ 1.4)

- GRE is a **tunneling protocol** used to encapsulate a wide variety of network layer protocols (Layer 3).
- It creates a virtual point-to-point link over an Internet Protocol (IP) network.
- GRE tunnels operate at **Layer 3 (Network Layer)** of the OSI model.
- They are configured on routers.

✅ **Why Use GRE?**
- **Protocol Translation:** Acts as a "universal translator" allowing different network protocols and technologies to communicate and traverse a shared network infrastructure, especially useful for connecting heterogeneous networks.
- **Connecting Branch Offices:** Enables the creation of a private and direct link over a public internet connection (e.g., connecting two branch offices without expensive leased lines).
- **Data Integrity & Confidentiality (Encapsulation):** Forms a "protective bubble" around data packets, isolating them from other internet traffic and maintaining their integrity and confidentiality during transit.

✅ **GRE vs. VPN (Virtual Private Network)**
- **GRE:**
  - Favored for its **simplicity and efficiency** in encapsulating multiple protocol types.
  - **Lightweight solution** for data encapsulation.
  - Does **NOT** provide encryption by itself.
- **VPN:**
  - Provides **robust security features**, including encryption.
  - Can be more complex and introduce more overhead due to encryption.

✅ **Combining GRE and VPN**
- For highly secure and encrypted communications over untrusted networks (like the internet), GRE can be combined with VPN technology.
- This provides both the **encapsulation** benefits of GRE and the **encryption** benefits of VPN.