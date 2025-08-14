## 💡 Layer 3: Network Layer (OBJ 1.1)

The Network Layer (Layer 3) is concerned with **routing** using **logical addresses** (e.g., IP addresses). Remember that IP and routers are the most common examples of Layer 3.

✅ **Layer-3 Switching (Routing)**
- The function of routing is sometimes referred to as layer-3 switching.
- A physical switch is typically a Layer 2 device, unless specified as a "multi-layer switch" (which operates at Layer 3).

✅ **Route Discovery and Selection**
- How routers determine the best path for traffic.
- Routers maintain **routing tables**.
- Routes can be **static** or **dynamically assigned** using routing protocols (e.g., RIP, OSPF, EIGRP).

✅ **Switching Methods**
- **Packet Switching:** Data is divided into packets, each forwarded independently based on its IP address. Most common method used on the internet and home networks. (Analogy: sending a letter where each part might take a different route).
- **Circuit Switching:** A dedicated communication link is established between two devices for the duration of the communication. (Analogy: a phone call where the path remains constant).
- **Message Switching:** Data is divided into messages that can be stored and forwarded (like email). Offers store-and-forward capability.

✅ **Connection Services**
- **Flow Control:** Prevents the sender from overwhelming the receiver.
- **Packet Reordering:** Allows packets that arrive out of order to be reassembled correctly at the destination.

✅ **ICMP (Internet Control Message Protocol)**
- Used to send messages and operational information to an IP destination.
- **Ping:** A common ICMP tool used to test connectivity and measure round-trip time.
- **Traceroute:** Uses ICMP to trace the path a packet takes through a network, identifying each router along the way.

✅ **Layer 3 Devices/Protocols**
- **Routers:** Primary Layer 3 devices.
- **Multi-layer Switches:** Devices that combine Layer 2 switching and Layer 3 routing capabilities.
- **IPv4 and IPv6:** Logical addressing protocols.
- **ICMP:** Protocol for network diagnostics.