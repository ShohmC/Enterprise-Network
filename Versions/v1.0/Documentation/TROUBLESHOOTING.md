# Version 1.0 - Problems & Troubleshooting

## Summary

Like any project, problems arose that had to be solved. They mainly were situations where I couldn't ping hosts on external VLANs but thankfully they were easy to troubleshoot for the most part.

## Problem 1: ASW1 wasn't forwarding any traffic
This was an easy problem to solve. I neglected to enable ip routing on the L3 switch which caused packets to drop as there was no routing enabled. Thankfully, a quick look at my notes made me realize this issue

## Problem 2: VLAN 10's PC1 wasn't pinging anything
This was also a very easy fix. I mistakenly input the wrong IP address for PC1, so a quick revision with ipconfig made me realize the issue

## Problem 3: VLAN 30 couldn't connect anywhere
This was probably the worst problem I had by far and took a lot of trail and error to figure out. I tried making sure all my default gateways and IPs were configured properly. Then I moved onto checking if my access ports were actually access ports. Then I checked my trunk connection and VLANs connected to the trunk. I tried resetting the network, I tried redoing my SVIs. The only thing that worked was chaning my native VLAN from the default to an unused one. This was mainly just trial and error, and following best practices, but I assume the main reason this was the fix was because VLAN 30 wasn't explicitely connected to any interface on the L3 switch, only the L2 one, so it was being sent untagged through VLAN 1, and since VLAN 1 is technically in use, it wasn't going anywhere.
