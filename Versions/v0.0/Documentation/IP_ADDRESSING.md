# Version 0.0 – IP Address Changes

## Summary

Configured IPv4 addresses for all end hosts and router interfaces.

## Addressing

| Device | Interface | IP Address | Subnet Mask |
|---------|-----------|------------|-------------|
| PC0 | NIC | 192.168.0.1 | 255.255.255.0 |
| PC1 | NIC | 192.168.0.2 | 255.255.255.0 |
| PC2 | NIC | 192.168.0.3 | 255.255.255.0 |
| PC3 | NIC | 192.168.1.1 | 255.255.255.0 |
| R1 | G0/0 | 192.168.0.254 | 255.255.255.0 |
| R1 | G0/1 | 192.168.1.254 | 255.255.255.0 |

## Notes

The 192.168.0.0/24 network is connected to R1's G0/0 interface.
The 192.168.1.0/24 network is connected to R1's G0/1 interface.
Router interfaces use `.254` as the default gateway for each subnet.
