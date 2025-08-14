## 💡 Transmission Control Protocol (TCP) (OBJ 1.4)

TCP is a fundamental protocol in the Internet Protocol Suite that ensures **reliable delivery** of data packets across a network. Remember that TCP is **reliable** and **connection-oriented**, using the three-way handshake and acknowledgements to ensure data integrity. Understand the role of ports in TCP communication.

✅ **TCP Overview**
- **Purpose:** Ensures **reliable delivery** of data packets across a network.
- **Reliability Achieved Through:** Error checking, data sequencing, and acknowledgements.
- **Operation:** Operates at the **Transport Layer (Layer 4)** of the OSI model.
- **Function:** Breaks larger messages into smaller packets, sends them, and reassembles them at the destination.

✅ **Three-Way Handshake**
- Used to **establish a connection** between two systems (client and server).
- **Steps:**
  - **1. SYN (Synchronize):** Client sends a SYN packet to initiate communication.
  - **2. SYN-ACK (Synchronize-Acknowledge):** Server responds with a SYN-ACK packet to acknowledge SYN and indicate willingness to establish a session.
  - **3. ACK (Acknowledge):** Client sends an ACK packet to confirm connection establishment.
- Ensures both sender and receiver are ready for data transmission.

✅ **Error Checking and Flow Control**
- **Sequence Numbers and Acknowledgements:** Used to ensure data is received correctly and in the proper order. Lost or corrupted packets are retransmitted.
- **Flow Control:** Prevents the sender from overwhelming the receiver.
- **Windowing:** Receiver specifies the amount of data it can handle at once. The "window" can be adjusted (widened/narrowed) based on network conditions.

✅ **Ports in TCP**
- **Purpose:** Numerical identifiers that distinguish between different services or applications running on the same physical computer.
- Each TCP connection is identified by a pair of endpoint addresses (source IP + port, destination IP + port).
- **Example:** HTTPS uses Port 443 for secure web access.