## 💡 Layer 4: Transport Layer (OBJ 1.1)

The Transport Layer (Layer 4) is the dividing line between the upper and lower layers of the OSI model. Data types at this layer are **segments** (for TCP) and **datagrams** (for UDP). Understand the key differences between TCP (reliable, connection-oriented, higher overhead) and UDP (unreliable, connectionless, lower overhead).

✅ **TCP (Transmission Control Protocol)**
- **Connection-oriented** and **reliable**.
- Uses a **three-way handshake** (SYN, SYN-ACK, ACK) to establish a connection.
- Ensures delivery through **acknowledgements** and **retransmission** of dropped segments.
- Used for data that requires assured delivery (e.g., banking, websites, e-commerce).
- Features **segmentation** and **sequencing** to ensure data arrives in order.
- Has higher overhead due to reliability mechanisms.

✅ **UDP (User Datagram Protocol)**
- **Connectionless** and **unreliable**.
- No three-way handshake, no acknowledgements, no retransmission, no sequencing.
- "Fire-and-forget" method.
- Lower overhead, making it suitable for applications where some data loss is acceptable (e.g., audio/video streaming, online gaming).

✅ **Windowing**
- Allows clients to adjust the amount of data sent in each segment to optimize throughput.
- The "window" opens (sends more data) when retransmissions are low and closes (sends less data) when retransmissions are high.
- Aims to maximize bandwidth utilization with minimal retransmissions.

✅ **Buffering**
- Routers and other devices use memory (buffers) to temporarily store segments when network congestion occurs or bandwidth is not immediately available.
- Prevents segment loss by holding data until it can be transmitted.
- If buffers overflow, segments will be dropped.

✅ **Layer 4 Devices/Concepts**
- TCP and UDP protocols.
- WAN accelerators (can operate at L4 by compressing IP packets).
- Load balancers and firewalls (can operate at L4 by blocking/allowing specific ports and protocols).