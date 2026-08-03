# Version 0.0 – Switch Changes

## Summary

Added two access switches, connecting each LAN to its default gateway, and enabled PortFast on all access ports.

### SW1

- Connected to PC0, PC1, and PC2.
- Enabled PortFast on interfaces Fa0/1–3.
- Enabled Fa0/1-3 as access ports.
- Connected GigabitEthernet0/0 to R1's GigabitEthernet0/0 interface.

### SW2

- Connected to PC3.
- Enabled PortFast on interface Fa0/1.
- Enabled Fa0/1 as an access port.
- Connected GigabitEthernet0/0 to R1's GigabitEthernet0/1 interface.

## Notes

PortFast was enabled only on access ports, which also were only enabled to ports connects to end-hosts only.
