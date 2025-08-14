## 💡 Ethernet Issues (OBJ. 5.2)
This section covers common Ethernet issues, including problems indicated by LED status indicators and duplex mismatches, along with their symptoms and troubleshooting methods.

✅ **Ethernet Issues**
- **1. LED Status Indicators (on NICs and Switches):**
  - **Activity Light:**
    - Off: No link/connection established.
    - Solid Orange: Link/connection established.
    - Blinking Orange: Data activity occurring over the link.
  - **Link Speed Light:** (Colors/states may vary slightly by NIC, but general idea applies)
    - Off: 10 Mbps connection.
    - Orange: 100 Mbps connection.
    - Green: 1 Gbps connection.
  - **Use:** Quick visual diagnostic tool to check link status and speed.
- **2. Duplexing Issues:**
  - **Duplex Mismatch (Most Common):**
    - **Definition:** Occurs when two ends of an Ethernet connection are configured differently (e.g., one is full-duplex, the other is half-duplex).
  - **Symptoms:**
    - High rate of packet loss (without high jitter, which would indicate congestion).
    - High receive error rate.
    - Presence of "runt" packets (frames smaller than minimum size).
  - **Prevention/Resolution:**
    - Ensure both devices are configured to use **auto-negotiate** for establishing connections.
    - If auto-negotiation fails, manually configure both ends to the same duplex setting (e.g., both to full-duplex if using a switch, as each switch port is its own collision domain).