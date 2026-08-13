# Version 1.0 – Subnet Changes
## Summary

Assigned subnets for each VLAN and P2P Connection to save address space within the 192.168.0.X space

## Subnets Created
| VLAN / Connection | Network Range                 | CIDR |
| ----------------- | ----------------------------- | ---- |
| VLAN 20           | 192.168.0.0 – 192.168.0.127   | /25  |
| VLAN 10           | 192.168.0.128 – 192.168.0.191 | /26  |
| VLAN 30           | 192.168.0.192 – 192.168.0.207 | /28  |
| VLAN 40           | 192.168.0.208 – 192.168.0.215 | /29  |
| ASW2 ↔ R1 P2P     | 192.168.0.216 – 192.168.0.219 | /30  |


## Notes

- More subnets will be added for different networks
- This is just one of many that will be added in the future