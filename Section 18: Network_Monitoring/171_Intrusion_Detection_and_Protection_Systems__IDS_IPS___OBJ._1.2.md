## 💡 Intrusion Detection and Protection Systems (IDS/IPS) (OBJ 1.2)

Intrusion Detection Systems (IDS) & Intrusion Prevention Systems (IPS) are network security devices that recognize and, in the case of IPS, respond to network attacks. They analyze incoming data for known attack patterns or suspicious behavior. Snort is a popular open-source, software-based IDS/IPS. Combining network-based and host-based IDS/IPS provides a multi-layered defense, offering comprehensive protection against various threats.

✅ **IDS vs. IPS: Detection vs. Prevention**
- **1. IDS (Intrusion Detection System):**
  - **Nature:** **Passive** device.
  - **Deployment:** Operates in parallel to the network (e.g., connected to a switch port in promiscuous mode).
  - **Function:** Monitors traffic, logs suspicious activity, captures packet data, and sends alerts to administrators.
  - **Action:** **Detects** attacks but does **NOT** actively block or stop them.
- **2. IPS (Intrusion Prevention System):**
  - **Nature:** **Active** device.
  - **Deployment:** Operates **in-line** with network traffic (all traffic must pass through it).
  - **Function:** Performs all IDS functions (monitoring, logging, alerting) PLUS actively **blocks or drops** offending traffic.
  - **Action:** Can **stop an attack in progress**.
  - **Trade-off:** Higher risk of **false positives** (blocking legitimate traffic) if not properly tuned, which is why some organizations prefer IDS.

✅ **Detection Methods**
- **1. Signature-Based Detection:**
  - **Mechanism:** Compares network traffic patterns against a database of known attack signatures (unique fingerprints of malicious activity).
  - **Analogy:** Like matching a known criminal's fingerprint.
  - **Limitation:** Only effective against known threats; cannot detect zero-day attacks.
- **2. Policy-Based Detection:**
  - **Mechanism:** Relies on a predefined security policy or set of rules (e.g., "No Telnet allowed on port 23").
  - **Action:** Flags any traffic that violates the established policy.
- **3. Anomaly-Based Detection:**
  - **Mechanism:** Builds a baseline of normal network behavior and flags any deviations from that baseline as suspicious.
  - **Types:**
    - **Statistical Anomaly:** Uses statistical analysis to identify unusual traffic patterns.
    - **Non-Statistical Anomaly:** Based on administrator-defined thresholds or patterns (e.g., "flag if a user downloads more than 1 GB per day").
  - **Challenge:** Can generate many false positives if the baseline is not accurate or if normal behavior changes.

✅ **Deployment Types: Host-Based vs. Network-Based**
- **1. Network-Based IDS/IPS (NIDS/NIPS):**
  - **Scope:** Protects an entire network segment.
  - **Deployment:** Dedicated network appliance or software running on a network device (e.g., router, firewall).
- **2. Host-Based IDS/IPS (HIDS/HIPS):**
  - **Scope:** Protects a single host (e.g., workstation, server, phone, tablet).
  - **Deployment:** Software installed directly on the individual host.
  - **Function:** Monitors local system calls, file changes, and application behavior.