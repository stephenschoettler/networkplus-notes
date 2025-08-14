## 💡 Encapsulation and Decapsulation (OBJ 1.1)

Encapsulation is the process of adding headers (and sometimes trailers) to data as it moves down the OSI layers (7 to 1). Decapsulation is the process of removing headers as data moves up the OSI layers (1 to 7). Remember the direction of encapsulation (down the layers) and decapsulation (up the layers).

✅ **Protocol Data Units (PDUs)**
- Single units of information transmitted in a network.
- **PDU Names:**
  - Layer 1: Bits
  - Layer 2: Frames
  - Layer 3: Packets
  - Layer 4: Segments (TCP) or Datagrams (UDP)

✅ **TCP Header (Layer 4)**
- Contains 10 mandatory fields (20 bytes).
- Important fields: Source Port, Destination Port, Sequence Number, Acknowledgement Number, Control Flags.
- **Control Flags:**
  - SYN: Synchronizes connection (three-way handshake).
  - ACK: Acknowledges successful receipt of packets.
  - FIN: Tears down virtual connection.
  - RST: Resets connection (e.g., unexpected packet, connection refused).
  - PSH (Push): Ensures data is given priority.
  - URG (Urgent): Identifies incoming data as urgent, processed immediately.

✅ **UDP Header (Layer 4)**
- Unreliable, connectionless protocol.
- Smaller header (8 bytes) with 4 fields: Source Port, Destination Port, Length, Checksum (optional).

✅ **IP Header (Layer 3)**
- Contains fields like IP version, header length, type of service, total length, source IP, destination IP.

✅ **Ethernet Header (Layer 2)**
- Contains Destination MAC address, Source MAC address, EtherType field (indicates encapsulated protocol like IPv4/IPv6), and optional VLAN tag.
- **MAC Address:** Physical address identifying a network card on a LAN, processed by switches.
- **EtherType:** Indicates the protocol encapsulated in the frame's payload.

✅ **Payload**
- The data being sent across the network.
- Minimum Ethernet payload: 42 bytes (with VLANs), 46 bytes (without VLANs).
- **Maximum Transmission Unit (MTU):** Default Ethernet MTU is 1500 bytes.
- **Jumbo Frame:** A frame larger than 1500 bytes, requires MTU reconfiguration on switches.

✅ **Data Flow Summary**
- Layer 7 to 1: Encapsulation (add headers: ports at L4, IPs at L3, MACs at L2).
- Layer 1: Transmit as bits.
- Receiving device (e.g., switch): Decapsulates L2, reads MAC. If not for it, forwards to default gateway (router).
- Router: Decapsulates L3, reads IP. If not for it, re-encapsulates and forwards.
- Final Host: Decapsulates all the way up to Layer 7 for the application to read.