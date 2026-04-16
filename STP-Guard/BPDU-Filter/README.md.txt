# 🔥 BPDU Filter Behavior Lab (STP)

This lab demonstrates the behavior of BPDU Filter in both interface-level and global (PortFast) configurations using GNS3.

---

## 🧩 Topology
![Topology](images/1_STP_Topology_Baseline.png)

- 3 Switches connected in triangle topology
- One switch acts as Root Bridge

---

## ⚠️ Interface BPDU Filter (Loop Risk)

![Interface BPDU Filter](images/2_Interface_BPDU_Filter_Loop_Risk.png)

- Applied BPDU filter on forwarding port
- BPDUs are not sent or received
- STP fails to detect loop
- All ports go into forwarding state

👉 Result: **Potential Layer 2 Loop**

---

## 💻 PortFast Edge Behavior (PC Connection)

![PortFast Edge](images/3_PortFast_Edge_PC_Connection.png)

- Port connected to PC
- PortFast enabled → Immediate forwarding
- No BPDU received

👉 Result: **Fast and stable edge port**

---

## 🔒 STP Loop Prevention (Switch Connection)

![STP Blocking](images/4_STP_Loop_Prevention_Blocking_State.png)

- Port connected to another switch
- BPDU received → PortFast disabled automatically
- STP recalculates topology
- One port moves to blocking state

👉 Result: **Loop-Free Network**

---

## 🧠 Key Learnings

- Interface BPDU Filter → Disables STP → Loop Risk
- Global BPDU Filter (PortFast) → Smart behavior → Safe
- STP dynamically adapts based on connection type

---