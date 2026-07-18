# Dynamic Host Configuration Protocol (DHCP)

## Overview

This lab demonstrates how a router can automatically assign network configuration to client devices using the Dynamic Host Configuration Protocol (DHCP).

Instead of manually configuring an IP address on every device, the router acts as a DHCP server and assigns the required network information whenever a client joins the network.

This project also uses Router-on-a-Stick (ROAS) to provide gateway connectivity between multiple VLANs.



## Objectives

- Configure a router as a DHCP server
- Create DHCP address pools for multiple VLANs
- Automatically assign IP addresses to client devices
- Verify successful IP assignment
- Understand how DHCP simplifies network administration



## Technologies Used

- Cisco Packet Tracer
- DHCP
- IPv4 Addressing
- VLANs
- Router-on-a-Stick (ROAS)



## Network Overview

The topology consists of:

- One Router
- One Switch
- Multiple VLANs
- Multiple Client Devices

Each VLAN has its own subnet and DHCP pool.

The router provides:

- Default Gateway
- DHCP Services
- Inter-VLAN Routing



## How DHCP Works

When a client device is configured to obtain an IP address automatically, it communicates with the DHCP server.

The router selects an available address from the configured DHCP pool and assigns network information to the client.

The assigned configuration includes:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

This removes the need to manually configure every device on the network.



## Verification

The configuration was verified by:

- Automatically assigning IP addresses to client devices
- Confirming network parameters on the clients
- Successful communication after receiving an IP address



## Key Takeaways

Through this lab I learned:

- How DHCP automates IP address management
- How routers function as DHCP servers
- How DHCP pools are configured for different networks
- The relationship between DHCP, VLANs and Router-on-a-Stick
- Why automatic IP assignment is essential for scalable network management



## Future Improvements

Future versions of this lab may include:

- DHCP Relay (IP Helper Address)
- DHCP across multiple routers
- OSPF Integration
- DNS Services
- Larger enterprise network deployments
