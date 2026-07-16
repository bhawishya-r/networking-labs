# Screenshot Explanation

This folder contains screenshots that verify the successful configuration of the Office Network project.



## VLAN Configuration (`vlans.png`)

This screenshot shows the VLANs created on the switch.

Configured VLANs:

| VLAN ID | Department |
|---------:|------------|
| 10 | Administration |
| 20 | Marketing |
| 30 | Sales |
| 40 | Canteen (Wireless) |

The output confirms that all required VLANs were successfully created and are active.



## Router Subinterfaces (`ip-interface.png`)

This screenshot shows the Router-on-a-Stick (ROAS) configuration.

Each VLAN is assigned its own router subinterface and default gateway.

| Interface | VLAN | Gateway |
|-----------|------|---------|
| GigabitEthernet0/1.10 | VLAN 10 | 192.168.1.1 |
| GigabitEthernet0/1.20 | VLAN 20 | 192.168.1.65 |
| GigabitEthernet0/1.30 | VLAN 30 | 192.168.1.129 |
| GigabitEthernet0/1.40 | VLAN 40 | 192.168.1.193 |

The interfaces are operational, allowing inter-VLAN communication through the router.



## RIP Configuration (`rip-configuration.png`)

This screenshot demonstrates the RIP routing configuration on the routers.

The connected networks were advertised using RIP, allowing routers to automatically exchange routing information without manually configuring static routes.



## Office Router Routing Table (`routing-table-office-router.png`)

Displays the routing table of the Office Router.

The learned RIP routes confirm successful exchange of routing information between routers.



## ISP Router Routing Table (`routing-table-isp-router.png`)

Shows the routing table on the ISP Router.

This verifies that routes from both the office network and server network have been learned correctly.



## Server Router Routing Table (`routing-table-server-router.png`)

Shows the routing table of the Server Router.

The router successfully learns routes to the office network through RIP.



## Successful End-to-End Ping (`successful-ping.png`)

This screenshot verifies successful communication between devices located on different VLANs and across different networks.

Successful replies confirm that:

- VLAN configuration is correct.
- Inter-VLAN routing is working.
- RIP has exchanged routes successfully.
- End-to-end connectivity has been established.



## Conclusion

These screenshots validate that the complete network is functioning as intended.

The project demonstrates:

- VLAN segmentation
- Subnetting
- Router-on-a-Stick (ROAS)
- Dynamic Routing using RIP
- Inter-VLAN Communication
- End-to-End Network Connectivity
