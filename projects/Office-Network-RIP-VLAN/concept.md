# Office Network using VLANs, Inter-VLAN Routing (ROAS) and RIP

## Overview

This project simulates a small office network connected to a remote server through an ISP.

The objective was to combine multiple networking concepts into a single topology instead of testing each concept separately.

This project includes:

- VLAN segmentation
- Router-on-a-Stick (ROAS)
- Inter-VLAN Communication
- RIP Dynamic Routing
- VLSM / Subnetting
- Wireless Access Points
- Remote Server Connectivity



## Network Topology

The network consists of three routers:

- Office Router
- ISP Router
- Server Router

The office network is divided into multiple departments using VLANs.

Each department has its own subnet and default gateway while still being able to communicate with other VLANs through Router-on-a-Stick.

A remote server network is connected through an ISP router, allowing office devices to communicate outside the local network.



## VLAN Design

| Department | VLAN | Network |
|------------|------|----------------|
| Administration | VLAN 10 | 192.168.1.0/26 |
| Marketing | VLAN 20 | 192.168.1.64/26 |
| Sales | VLAN 30 | 192.168.1.128/26 |
| Canteen / Wireless | VLAN 40 | 192.168.1.192/26 |

Each VLAN is isolated at Layer 2 and uses its own default gateway.



## Inter-VLAN Routing

Inter-VLAN communication is implemented using Router-on-a-Stick (ROAS).

The router uses multiple subinterfaces, each configured with:

- VLAN encapsulation (802.1Q)
- Gateway IP address
- Corresponding subnet

This allows devices from different VLANs to communicate.



## Dynamic Routing

Routing Information Protocol (RIP Version 2) is configured between:

- Office Router
- ISP Router
- Server Router

Instead of manually configuring static routes, routers exchange routing information automatically.

This allows remote networks to become reachable without creating individual static routes.



## Remote Server

A separate server network is connected through the ISP router.

Office clients can successfully communicate with the server because:

- VLAN routing is handled by ROAS
- RIP advertises all networks
- Routers automatically build their routing tables



## What I Learned

Through this project I gained practical understanding of:

- Designing networks using subnetting
- VLAN segmentation
- Broadcast domain separation
- Router-on-a-Stick
- Trunk links
- Dynamic routing with RIP
- Route advertisement
- Multi-router communication
- End-to-end packet forwarding

This project combines multiple networking concepts into one practical topology, making it much closer to a real-world network than isolated labs.
