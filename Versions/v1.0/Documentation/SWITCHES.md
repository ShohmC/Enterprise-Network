# Version 1.0 – Switch Changes
## Summary

Configured a L2 and L3 switch to provide inter-VLAN connectivity throughout the network.

## ASW1 (L2)

- Connected:

  - VLAN 10 to Fa0/1–2
  - VLAN 20 to Fa0/3–4
  - VLAN 30 to Fa0/5–6
- Configured **Fa0/1–6** as access ports.
  - Enabled PortFast and BPDU Guard on each access port.
- Configured **Fa0/7** as an 802.1Q trunk allowing VLANs 10, 20, and 30.
- Configured **VLAN 1000** as the unused native VLAN.

> **Note:** Each VLAN contains placeholder groups of 2–4 hosts to represent the intended network size. The actual number of hosts is documented within the network topology.

## ASW2 (L3)

- Connected:

  - VLAN 10 to G1/0/1–2 
  - VLAN 20 to G1/0/3–4 
  - VLAN 40 to G1/0/5–6 
- Configured **G1/0/1–6** as access ports.

  - Enabled PortFast and BPDU Guard on each access port.
- Configured **G1/0/7** as an 802.1Q trunk allowing VLANs 10, 20, and 30.
- Configured **VLAN 1000** as the used native VLAN.
- Created the following Switch Virtual Interfaces (SVIs):

  - **VLAN 10:** `192.168.0.190/26`
  - **VLAN 20:** `192.168.0.126/27`
  - **VLAN 30:** `192.168.0.206/28`
  - **VLAN 40:** `192.168.0.215/29`
- Configured each SVI as the default gateway for its respective VLAN.
- Established a point-to-point connection to R1 (G0/0) using G1/0/8 within the 192.168.0.216/30 subnet.

  - Assigned ASW2 G1/0/8 the IP address 192.168.0.217/30.

## Notes

- This version uses SVIs on the Layer 3 switch to perform inter-VLAN routing.
- VLAN 1000 is reserved as an unused native VLAN to reduce the risk of VLAN hopping attacks.


