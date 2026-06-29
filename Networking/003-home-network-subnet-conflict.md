# Home Network Subnet Conflict (192.168.1.1 → 10.10.1.1)

## Environment

Home lab using a UniFi Cloud Gateway Ultra connected to an ISP modem/router.

## Symptoms

* Internet connectivity was unavailable after installing the UniFi gateway.
* Both the ISP modem/router and the UniFi gateway were using the same LAN subnet (192.168.1.0/24).
* Management access and routing behavior were inconsistent due to overlapping networks.

## Troubleshooting

* Verified WAN and LAN connections.
* Checked the LAN IP addresses of both the ISP modem/router and the UniFi gateway.
* Identified that both devices were configured for the 192.168.1.0/24 subnet.
* Changed the UniFi gateway LAN network to 10.10.1.0/24.
* Updated client devices to obtain new IP addresses.

## Root Cause

The ISP modem/router and the UniFi gateway were configured on the same LAN subnet, creating a subnet conflict that prevented proper routing.

## Solution

Changed the UniFi gateway LAN IP from **192.168.1.1** to **10.10.1.1**, creating a separate internal network. Once clients received addresses in the new subnet, connectivity was restored.

## Lessons Learned

* Avoid overlapping LAN subnets between upstream and downstream routers.
* Always verify IP addressing before troubleshooting routing issues.
* Using a dedicated private subnet (such as 10.10.1.0/24) simplifies future VLAN and home lab expansion.
