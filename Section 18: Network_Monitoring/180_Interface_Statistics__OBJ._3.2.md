## 💡 Interface Statistics (OBJ 3.2)

Interface Statistics are used to monitor network performance and troubleshoot issues by examining data from physical or logical switch ports (interfaces) on network devices.

✅ **Key Metrics to Understand (for the exam)**
- **1. Link State:**
  - `up/up`: Interface is physically connected and protocol is operational (frames can enter/leave).
  - `down/down`: No physical connection or protocol issue.
- **2. Speed and Duplex Status:**
  - Indicates the connection speed (e.g., 100 Mbps) and duplex mode (Half or Full).
  - **Full Duplex:** Allows simultaneous send/receive; no collisions should occur.
  - **Half Duplex:** Send or receive at one time; collisions can occur.
  - **Troubleshooting:** Half-duplex on a switch port can cause slowdowns (effectively halves bandwidth).
- **3. Send/Receive Traffic Statistics:**
  - **Input/Output Rates:** Average rates of packets being received/transmitted.
  - **Packet/Byte Counts:** Total number of packets and bytes processed.
  - **TxLoad/RxLoad:** How busy the router is transmitting/receiving frames.
- **4. Cyclic Redundancy Check (CRC) Statistics:**
  - **CRC Errors:** Number of packets received that failed the CRC checksum.
  - **Troubleshooting:** High CRC errors indicate data corruption (noise, bad cabling, EMI, dirty fiber connectors).
- **5. Protocol Packet and Byte Counts:**
  - **Runts:** Ethernet frames smaller than 64 bytes.
  - **Giants:** Ethernet frames larger than 1518 bytes.
  - **Input Errors:** General counter for frames received with any error.
  - **Output Errors:** General counter for frames transmitted with errors.
  - **Collisions:** Number of times a packet needed retransmission due to Ethernet collision. Should be zero on full-duplex.
  - **Drops:** Packets discarded (e.g., due to full queues, congestion).
  - **Ignored:** Packets ignored due to low internal buffers (can indicate noise/broadcast storm).
  - **Underruns:** Sender operates faster than receiver, causing buffer issues.
  - **Overruns:** Interface unable to receive traffic due to insufficient hardware buffer.
  - **Unknown Protocol Drops:** Packets dropped because the protocol is unrecognized.
- **6. Queuing Strategy:**
  - How packets are handled in queues (e.g., FIFO - First In, First Out).
  - Queue size and drops indicate congestion.
- **7. Last Input/Output/Clear:** Timestamps of last activity or counter reset.

✅ **Troubleshooting Scenarios**
- **Slow Device:** Check for half-duplex (should be full), high collision count (indicates issues like a hub connected to a switch port).
- **CRC Errors:** Suspect dirty fiber, EMI, bad cabling.
- **High Drops/Ignored:** Indicates congestion or noise/broadcast storms.