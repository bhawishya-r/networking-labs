# Spanning Tree Protocol (STP) Lab

## Objective

Build a switched network with redundant paths and observe how Spanning Tree Protocol prevents Layer 2 loops by placing redundant links into a blocking state.



## Network Topology

<img width="1099" height="580" alt="STP-topology" src="https://github.com/user-attachments/assets/197b62c1-60b9-4e96-ac17-75c72e80d78a" />




## Devices Used

- Cisco Switches
- PCs
- Copper Straight-through Cables
- Copper Cross-over cables



## Concepts Practiced

- Layer 2 Switching
- Redundant Links
- Root Bridge
- Root Port
- Designated Port
- Blocking Port
- Loop Prevention



## Verification

✔ STP elected a Root Bridge

✔ One redundant link entered Blocking State

✔ End devices maintained connectivity

✔ Broadcast loops were prevented



## Files

- STP-Lab.pkt
- topology.png



## What I Learned

- Layer 2 loops can create broadcast storms.
- STP prevents loops without disconnecting redundant links.
- Switches automatically elect a Root Bridge.
- Redundant paths remain available if the active path fails.



## My Takeaway

> Redundancy increases reliability, but without STP it can also create loops. STP balances both by keeping backup paths ready while preventing broadcast storms.
