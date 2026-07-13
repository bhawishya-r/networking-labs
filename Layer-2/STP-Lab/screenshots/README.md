# Spanning Tree Protocol (STP) Lab

## Objective

The objective of this lab was to understand how Spanning Tree Protocol (STP) prevents switching loops by electing a Root Bridge, assigning port roles, and blocking redundant paths while maintaining network connectivity.



## Network Topology

The topology consists of three interconnected Cisco 2960 switches, creating a Layer 2 loop. STP automatically selects one switch as the Root Bridge and blocks one redundant link to eliminate broadcast storms.

<img width="1099" height="580" alt="STP-topology" src="https://github.com/user-attachments/assets/3312d37a-ca87-48f7-8cbd-e8dffb7d6911" />


**Observations**
- Three switches form a triangular topology.
- Switch4 was elected as the Root Bridge.
- One redundant port entered the Blocking state to prevent loops.
- End devices remained connected while redundant paths were preserved as backups.



## Root Bridge Election

The output below confirms that **Switch4** became the Root Bridge.

<img width="581" height="249" alt="spanning-tree-root" src="https://github.com/user-attachments/assets/f25d82c7-3db2-4497-8530-e8eb51cd0e81" />


**Key Observations**
- "This bridge is the root" confirms the switch is the Root Bridge.
- All ports on the Root Bridge are Designated Ports.
- Every port remains in the Forwarding state because the Root Bridge never blocks its own interfaces.



## Port Roles and Blocking Port

The following output was captured from **Switch2**.

<img width="582" height="328" alt="root-interface" src="https://github.com/user-attachments/assets/e922a034-d758-4c20-b281-3f1f7ba9cadd" />


**Key Observations**
- **Fa0/3** is selected as the **Root Port** because it provides the lowest-cost path to the Root Bridge.
- **Fa0/1** becomes a **Designated Port**.
- **Fa0/2** is placed into the **Alternate Blocking** state.
- The blocked port prevents Layer 2 loops while remaining available as a backup path.



## What I Learned

- Why Layer 2 loops occur.
- How STP elects the Root Bridge.
- Bridge ID (Priority + MAC Address).
- Root Ports, Designated Ports, and Alternate Ports.
- Path Cost calculation.
- Port States (Forwarding and Blocking).
- Redundant path prevention without physically disconnecting cables.
- Using the `show spanning-tree` command to verify STP operation.



## Commands Used

```bash
show spanning-tree
show running-config
```



## Skills Practiced

- Cisco Packet Tracer
- Layer 2 Switching
- Spanning Tree Protocol (IEEE 802.1D)
- Network Topology Design
- CLI Verification
- Network Troubleshooting
