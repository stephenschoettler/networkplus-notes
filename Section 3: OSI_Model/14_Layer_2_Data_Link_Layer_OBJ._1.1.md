## 💡 Layer 2: Data Link Layer (OBJ 1.1)

The Data Link Layer (Layer 2) packages bits into **frames** for transmission, performs error detection/correction, identifies unique devices using MAC addresses, and provides flow control. Remember that switches, bridges, and MAC addresses operate at Layer 2.

✅ **MAC (Media Access Control) Address**
- A unique 48-bit physical address assigned to every Network Interface Card (NIC).
- Written in 12-digit hexadecimal numbers.
- The first 24 bits (first 6 hex digits) identify the manufacturer (Organizationally Unique Identifier - OUI).
- The remaining bits uniquely identify the specific device.
- Important for logical topology and used by switches to identify devices.

✅ **Logical Link Control (LLC)**
- Provides connection services, allowing recipients to acknowledge message receipt.
- Offers basic **flow control** to prevent sender from overwhelming receiver.
- Provides basic **error control** using checksums to detect corrupted frames and request retransmission.

✅ **Communication Synchronization Schemes**
- **Isochronous Mode:** Uses a common reference clock and time slots for transmissions (less overhead).
- **Synchronous Mode:** Devices use the same clock, with special control characters for start/end frames.
- **Asynchronous Mode:** Each device uses its own clock, with start and stop bits (less control over communication timing).

✅ **Layer 2 Devices**
- **Network Interface Cards (NICs)**
- **Bridges**
- **Switches:** Smarter than hubs, they learn MAC addresses and forward data to specific devices based on MAC addresses.