## 💡 Internet Protocol Security (IPSec) (OBJ 1.4)

IPSec is a secure network protocol suite that provides authentication and encryption of data packets to create a secure, encrypted communication path between two computers over an IP network. Its primary use is for creating and operating VPNs (Virtual Private Networks), both site-to-site and client-to-site.

✅ **Security Features Provided**
- **Confidentiality:** Data encryption.
- **Integrity:** Ensures data was not modified in transit (by checking hashes).
- **Authentication:** Verifies the identity of each party.
- **Anti-Replay:** Prevents transmission of duplicate packets (by checking sequence numbers).

✅ **IPSec Phases (Key Exchange and Tunnel Establishment)**
- **1. IKE Phase 1 (Internet Key Exchange Phase 1):**
  - **Purpose:** Authenticates the IPSec peers and establishes a secure channel for negotiation (IKE SA - Security Association).
  - **Modes:**
    - **Main Mode:** More secure, involves three 2-way exchanges (6 packets).
    - **Aggressive Mode:** Faster, fewer exchanges (3 packets). Less secure.
  - **Outcome:** Both peers have a shared secret key and matching IKE SAs.
- **2. IKE Phase 2 (Internet Key Exchange Phase 2):**
  - **Purpose:** Negotiates IPSec Security Association (SA) parameters to set up the actual IPSec tunnel.
  - **Mode:** Uses Quick Mode.
  - **Mechanism:** Negotiates a shared IPSec policy and derives key materials, protected by the IKE SA from Phase 1.
  - **Outcome:** Establishes IPSec SAs for data transfer. SAs have limited lifespans and are periodically renegotiated (rekeying) to maintain security.

✅ **IPSec Data Transfer Modes**
- **1. Transport Mode:**
  - **Use:** Typically for client-to-site VPNs.
  - **Mechanism:** Uses the packet's original IP header. Encrypts only the payload (data) and optionally the TCP/UDP header.
  - **Benefit:** Does not add significant padding, so it's less likely to exceed MTU size.
  - **Limitation:** Original IP header is visible, so source/destination IPs are exposed.
- **2. Tunnel Mode:**
  - **Use:** Typically for site-to-site VPNs.
  - **Mechanism:** Encapsulates the entire original IP packet (header + payload) within a new IP packet. Adds a new IP header.
  - **Benefit:** Provides end-to-end confidentiality; original source/destination IPs are hidden from intermediate networks.
  - **Limitation:** Increases packet size, potentially exceeding MTU. May require allowing "jumbo frames" or adjusting MTU.

✅ **IPSec Components (Protocols)**
- **1. Authentication Header (AH):**
  - **Provides:** Connectionless data integrity, data origin authentication, and anti-replay protection.
  - **Does NOT provide:** Confidentiality (no encryption of data).
  - **Mechanism:** Adds a cryptographic hash of the data to the packet.
- **2. Encapsulating Security Payload (ESP):**
  - **Provides:** Authentication, integrity, anti-replay protection, AND confidentiality (encryption) of the data.
  - **Mechanism:** Encrypts the payload and optionally the TCP/UDP header.
  - **Use with Modes:**
    - **Transport Mode:** Encrypts payload and TCP/UDP header. Original IP header remains visible.
    - **Tunnel Mode:** Encrypts the entire original packet (including its header) and adds a new IP header. Hides original source/destination.