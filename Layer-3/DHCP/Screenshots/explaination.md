# Screenshot Explanation

This folder contains screenshots demonstrating the successful configuration and verification of the DHCP lab.



## Network Topology 

Displays the complete network topology used in this lab.

The topology consists of:

- One Router
- One Switch
- Multiple VLANs
- Client Devices

The router acts as both the DHCP server and the Router-on-a-Stick (ROAS) device for inter-VLAN communication.



## DHCP Configuration 

Shows the DHCP pools configured on the router.

Each DHCP pool is configured with:

- Network Address
- Subnet Mask
- Default Gateway

These settings allow the router to automatically assign network configuration to clients within their respective VLANs.



## DHCP Address Assignment 

Shows a client device requesting an IP address automatically.

The client successfully receives:

- IP Address
- Subnet Mask
- Default Gateway

This confirms that the DHCP server is functioning correctly.




## Connectivity Verification (`successful-ping.png`)

Shows successful communication after DHCP configuration.

Successful ping replies verify that:

- The client received a valid IP address.
- The default gateway is reachable.
- Network communication is functioning correctly.



## Conclusion

These screenshots confirm the successful implementation of:

- Dynamic Host Configuration Protocol (DHCP)
- Automatic IP Address Assignment
- Router-on-a-Stick (ROAS)
- VLAN-based Network Configuration

The lab demonstrates how DHCP simplifies network administration by automatically providing devices with the network settings required for communication.
