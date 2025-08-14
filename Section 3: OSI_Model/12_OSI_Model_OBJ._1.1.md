## 💡 OSI Model (OBJ 1.1)

The OSI (Open Systems Interconnection) model, also known as the OSI Stack, was developed in 1977 by the International Organization for Standardization (ISO). It is a **reference model** used to categorize network functions and aid in troubleshooting. While it doesn't perfectly align with modern networks, which primarily use the TCP/IP model, it's still crucial for understanding network concepts and troubleshooting.

✅ **Seven Layers of the OSI Model**
- The OSI model has **seven layers**, which must be memorized in order (bottom-to-top and top-to-bottom) for the exam.
- **Layers (Bottom to Top):**
  - **1. Physical**
  - **2. Data Link**
  - **3. Network**
  - **4. Transport**
  - **5. Session**
  - **6. Presentation**
  - **7. Application
- **Mnemonic (bottom to top):** "Please Do Not Throw Sausage Pizza Away" (Physical, Data Link, Network, Transport, Session, Presentation, Application).

✅ **Data Naming Conventions**
- Data is named differently as it moves down the layers:
  - Layers 5, 6, 7: **Data**
  - Layer 4 (Transport): **Segment**
  - Layer 3 (Network): **Packet**
  - Layer 2 (Data Link): **Frame**
  - Layer 1 (Physical): **Bits**
- **Mnemonic (top to bottom):** "Do Some People Fear Birthdays?" (Data, Segment, Packet, Frame, Bits).

✅ **Encapsulation and Decapsulation**
- **Encapsulation:** The process of wrapping data with protocol information at each layer as it moves *down* the networking stack.
- **Decapsulation:** The process of removing protocol information layer by layer as data moves *up* the OSI model on the receiving end.

✅ **Wireshark**
- A network protocol analyzer used to capture and display data, useful for inspecting, troubleshooting, and analyzing how data is broken down into OSI layers.