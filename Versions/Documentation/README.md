# Version 1.0 - Overview

## Summary

Implemented my first small-scale network topology which consists of multiple VLANs connected together with a L2 and L3 switch while utilizing SVIs as the default gateway.

## New Features

- Added multiple VLANs (10, 20, 30, 40).
  - Subnetted the VLANs to keep them all within a 192.168.0.x address space.
  - Added multiple hosts to each VLAN and configured a static IP address, subnet, and default gateway.
- Added switches ASW1 (L2) and ASW2 (L3).
  - Configured PortFast and BPDU Guard on all access ports.
  - Created SVIs for each VLAN.
- Added router R1.

## Changes
 
- Brand new topology, no changes to existing infrastructure can be made.

## Future Plans
- Connecting a secondary physical LAN to the main network, and providing Inter-VLAN routing on the secondary LAN using Router-on-a-Stick (ROAS).
- Configure EtherChannel between switches for increased bandwidth and redundancy.
