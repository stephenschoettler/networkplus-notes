## 💡 Datacenter Topology (OBJ 1.6)

A **datacenter** is a facility with networked computers and storage used by organizations to organize, process, store, and disseminate large amounts of data.

✅ **Datacenter Topologies**
- **1. Three-tiered Hierarchy:**
  - Consists of three layers: Core, Distribution/Aggregation, and Access/Edge.
  - **Core Layer:**
    - Backbone of the network, merging geographically separated networks.
    - Uses the biggest, fastest, most expensive routers.
    - Typically has redundant routers (at least two).
  - **Distribution/Aggregation Layer:**
    - Provides boundary definition, implementing access lists and filters.
    - Defines policies for networks.
    - Often uses Layer 3 switches.
  - **Access/Edge Layer:**
    - Connects all endpoint devices (computers, servers, printers, WAPs).
    - Usually uses regular switches.
    - Converts packets to frames and delivers to correct endpoints.
  - Benefits: Better performance, management, scalability, redundancy, and easier troubleshooting.
- **2. Collapsed Core:**
  - A two-tiered system where the **Core and Distribution layers are merged** into a single layer.
  - Simplifies architecture, reduces number of switches, lowers costs, and reduces latency (fewer hops).
  - Often used in smaller to medium-sized datacenters where full three-tiered scalability isn't required.
- **3. Spine and Leaf Architecture:**
  - Alternative architecture used specifically *within* datacenters, especially for server farms.
  - Consists of two switching layers: **Spine** and **Leaf**.
  - **Leaf Layer:** Access switches that aggregate traffic from servers and connect directly to the Spine layer.
  - **Spine Layer:** Interconnects all Leaf layer switches in a full mesh topology, acting as the backbone.
  - Benefits: Increased performance and redundancy, lower latency (due to full mesh connectivity).
  - Often involves "top of rack" switching, where two switches are installed at the top of each server rack.
  - Can be combined with a traditional three-tiered hierarchy (Spine connects to the Core layer).

✅ **Traffic Flows in Datacenters**
- **1. North-South Traffic:**
  - Traffic that **enters or leaves** the datacenter from systems physically residing *outside* the datacenter.
  - **Northbound Traffic:** Exiting the datacenter.
  - **Southbound Traffic:** Entering the datacenter.
  - Typically passes through firewalls or other network infrastructure boundaries (e.g., routers).
- **2. East-West Traffic:**
  - Traffic flow **within** the datacenter (e.g., communication between servers in the same datacenter).
  - Due to increased use of SDN, virtualization, and cloud, more traffic is becoming East-West.

✅ **Exam Tip**
- The choice of datacenter topology depends on specific business needs and organizational size.