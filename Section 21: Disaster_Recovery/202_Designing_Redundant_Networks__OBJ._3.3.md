## 💡 Designing Redundant Networks (OBJ. 3.3)
This section focuses on the principles of designing redundant networks, emphasizing the balance between cost, availability, and reliability, and exploring various types of redundancy and best practices.

✅ **Designing Redundant Networks**
- Balancing cost, availability, and reliability is key.

✅ **Types of Redundancy**
- **Hardware:**
  - Module/Parts: Redundant power supplies, NICs, hard drives (cost-effective).
  - Chassis: Redundant routers/switches (more expensive).
- **Software:** Virtual devices, software RAID (cost-effective alternatives).
- **Protocol:** TCP (retransmission) vs. UDP (no retransmission).
- **Power:** Internal PSUs, UPS, generators.
- **Environmental:** Redundant cooling (AC units), space.

✅ **Business Case is Crucial**
- Justify all redundancy decisions based on organizational needs and budget.
- Needs vary by organization size and criticality.

✅ **Best Practices & Goals**
- **Technical Goals:** Define target uptime (e.g., "five nines" of availability).
- **Operational Goals:** Categorize applications for QoS (Quality of Service).
- **Performance Standards:** Establish metrics (KPIs) to measure success.
- **Metrics:** Quantify success for decision-makers; ensure they align with desired outcomes.

✅ **Key Takeaway**
- **Design Redundancy Early:** Much cheaper to build in from scratch than to retrofit.
- **Project Triangle (Time, Cost, Quality):** You can't have all three perfectly. Redundancy improves quality but impacts time/cost.