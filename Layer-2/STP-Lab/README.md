# Spanning Tree Protocol (STP) Lab

## Objective

Build a switched network with redundant paths and observe how Spanning Tree Protocol prevents Layer 2 loops by placing redundant links into a blocking state.



## Network Topology

(Add topology image here)



## Devices Used

- Cisco Switches
- PCs
- Copper Straight-through Cables



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
