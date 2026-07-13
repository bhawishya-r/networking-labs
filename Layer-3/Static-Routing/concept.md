# Static Routing Lab

## Overview

This lab demonstrates communication between two separate LANs using static routing across three Cisco routers.

The objective was to understand how routers forward packets between different networks by using manually configured routing tables.

Rather than relying on dynamic routing protocols, every route in this topology was configured manually to better understand how routers make forwarding decisions.



## Network Topology

The network consists of:

- 2 Local Area Networks (LANs)
- 3 Cisco Routers
- 2 Switches
- 4 PCs

Each LAN is connected through a router, while a third router acts as the transit router connecting both networks.

<img width="998" height="632" alt="topology-static-r" src="https://github.com/user-attachments/assets/967375cc-a503-46e9-a033-6fe0b21cc4ac" />




## IP Addressing

| Device | Network |
|---------|----------|
| LAN-1 | 192.168.10.0/24 |
| Router1 ↔ Router0 | 192.168.20.0/24 |
| Router0 ↔ Router2 | 192.168.30.0/24 |
| LAN-2 | 192.168.40.0/24 |



## Objective

- Configure router interfaces
- Configure static routes
- Understand routing tables
- Learn next-hop routing
- Verify end-to-end communication
- Understand default gateways
- Observe packet forwarding across multiple routers



## Configuration Steps

### 1. Configure IP addresses

Configured IP addresses for:

- Router interfaces
- PCs
- Default gateways



### 2. Configure Static Routes

Each router was manually configured with routes to reach remote networks.

Example:

```
ip route <Destination Network> <Subnet Mask> <Next-Hop IP>
```

---

### 3. Verify Routing Tables

Verified configured routes using:

```
show ip route
```

This confirms whether routers know how to reach remote networks.

---

### 4. Test Connectivity

Connectivity was verified using:

```
ping
```

Packets successfully traveled:

```
PC
↓

Switch
↓

Router 1
↓

Router 0
↓

Router 2
↓

Switch
↓

Destination PC
```



## Packet Flow

When a PC sends data to another network:

1. The packet is sent to its Default Gateway.
2. Router1 checks its routing table.
3. The packet is forwarded to Router0.
4. Router0 forwards it to Router2.
5. Router2 recognizes the destination network as directly connected.
6. The packet reaches the destination PC.



## What I Learned

- Layer 3 packet forwarding
- Static Routing
- Routing Tables
- Next-Hop Routing
- Default Gateway
- Router Interfaces
- Longest Prefix Match
- End-to-End Communication
- Basic Network Design



## Commands Used

```bash
show ip route
show running-config
show ip interface brief
ping
```



## Skills Practiced

- Cisco Packet Tracer
- Router Configuration
- Static Routing
- Network Troubleshooting
- IP Address Planning
- Routing Table Verification
