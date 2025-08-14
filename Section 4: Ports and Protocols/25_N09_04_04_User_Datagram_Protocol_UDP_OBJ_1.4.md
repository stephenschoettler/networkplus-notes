## 💡 User Datagram Protocol (UDP) (OBJ 1.4)

UDP is a communication protocol used for **time-sensitive transmissions** where speed is more critical than guaranteed delivery (e.g., video playback, DNS lookups, online gaming, VoIP). Understand the core difference between UDP and TCP: UDP prioritizes speed and efficiency over reliability, while TCP prioritizes reliability over speed. Remember that UDP is connectionless and unreliable.

✅ **UDP Overview**
- **Purpose:** Used for **time-sensitive transmissions** where speed is more critical than guaranteed delivery.
- **Characteristics:**
  - **Low latency** and **reduced processing overhead**.
  - **Connectionless:** Sends data packets (called **datagrams**) to the recipient without prior connection setup (no three-way handshake).
  - **Unreliable:** Lacks error checking and recovery services of TCP. If packets are lost, the sender is unaware and does not retransmit.
  - **Stateless:** Does not maintain the state of the connection or track packets. Often called "fire-and-forget."
  - **Smaller Header:** UDP datagram headers are only 8 bytes (compared to TCP's 20-60 bytes), making it more efficient for speed.
  - **Checksum:** Includes a checksum for minimal protection against data corruption, but this does not make it a reliable protocol.

✅ **When to Use UDP**
- Applications where losing some packets is acceptable and preferable to delays (e.g., streaming video/audio, where a slight glitch is better than buffering).
- Simple request-response communications (e.g., DNS lookups).

✅ **Ports in UDP**
- UDP uses ports (source and destination) in its header to direct datagrams to the correct application process on the receiving end.