# Screenshot Explanation

This document explains the purpose of each screenshot included in this lab and what it demonstrates.


## 1. Network Topology


Shows the complete network topology used for this lab.

The network consists of:

- Three Cisco routers
- Two Layer 2 switches
- Four end devices
- Two separate LANs connected through a transit router

This topology was created to demonstrate how static routing enables communication between different IP networks.



## 2. Router0 Routing Table


This screenshot displays the routing table of the middle router.

It verifies that:

- Directly connected networks are present.
- Static routes have been configured correctly.
- Router0 knows where to forward packets destined for remote networks.

Router0 serves as the transit router between both LANs.



## 3. Router1 Routing Table


Shows the routing table of Router1.

This confirms that Router1 has a static route pointing toward the remote network (LAN-2) using Router0 as the next hop.



## 4. Router2 Routing Table


Displays the routing table of Router2.

The screenshot verifies that Router2 has a static route configured toward LAN-1 through Router0.


## 5. Successful End-to-End Ping


This screenshot verifies successful communication between two different LANs.

The source device sends ICMP Echo Requests to a host located in another network.

Although the first packet times out, the remaining packets receive replies successfully.

This behavior is expected because the first packet triggers ARP resolution before communication begins.

The successful replies confirm that:

- IP addressing is correct.
- Default gateways are configured properly.
- Static routes are functioning.
- All routers are forwarding packets correctly.
- End-to-end connectivity has been established.



## Summary

These screenshots collectively verify every major component of the lab:

- Network topology
- Static route configuration
- Routing table verification
- Packet forwarding
- Successful communication between different networks

Together, they demonstrate a fully functional static routing implementation using Cisco Packet Tracer.
