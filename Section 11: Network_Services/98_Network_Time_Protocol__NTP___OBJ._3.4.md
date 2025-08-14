## 💡 Network Time Protocol (NTP) (OBJ 3.4)

NTP is a networking protocol used for the **synchronization of clocks** between different computer systems over a packet-switched, variable-latency data network (like TCP/IP networks). While NTP is foundational, PTP offers higher precision for demanding applications, and NTS adds crucial security to time synchronization processes.

✅ **NTP Overview**
- **Purpose:** Synchronizes the clocks of computer systems over a network.
- **Key Features:**
  - Very old protocol, still widely used.
  - Uses UDP packets on **port 123**.
  - Aims to synchronize clocks to within a few milliseconds of **UTC (Coordinated Universal Time)**.
- **Importance:**
  - Many **security protocols** rely on accurate time (e.g., preventing login errors if workstation and server time are off).
  - Crucial for **logging, troubleshooting, and proper functioning** of many applications.

✅ **NTP Hierarchy: Stratum Levels**
- NTP uses a hierarchical system of time sources, with each layer known as a **stratum**. Lower stratum numbers indicate higher precision and closer proximity to the original time source.
- **Stratum 0 (Reference Clocks):** Most precise timekeeping devices (e.g., atomic clocks, GPS receivers). These are not NTP servers themselves but provide the highly accurate time source.
- **Stratum 1 (Primary Time Servers):** NTP servers directly synchronized to a Stratum 0 reference clock.
- **Stratum 2:** NTP servers synchronized to a Stratum 1 server.
- **Stratum 3 and higher:** Servers synchronized to a lower stratum server. Each step introduces a slight delay.
- **Limit:** The maximum stratum level is 15.
- **Stratum 16:** Indicates an unsynchronized device.

✅ **Newer Time Synchronization Protocols**
- **1. PTP (Precision Time Protocol)**
  - **Purpose:** Provides **sub-microsecond accuracy** for clock synchronization.
  - **Use Cases:** Ideal for networks requiring extreme precision (e.g., financial trading, industrial automation).
  - **Mechanism:** Operates using a primary-secondary architecture, with the primary clock sending precise time messages and secondary clocks adjusting.
- **2. NTS (Network Time Security)**
  - **Purpose:** An **extension of NTP** designed to provide **cryptographic security** for time synchronization.
  - **Problem Addressed:** NTP is vulnerable to various attacks (e.g., on-path attacks) that could tamper with time information.
  - **Mechanism:** Uses TLS (Transport Layer Security) and AEAD (Authenticated Encryption with Associated Data) to authenticate the time source and ensure the integrity of the time received.