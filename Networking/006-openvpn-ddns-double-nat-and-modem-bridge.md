# OpenVPN Remote Access - DDNS, Double NAT, and Modem Bridge

## Environment

Residential network using a router behind an ISP modem, with OpenVPN remote access and No-IP DDNS.

## Symptoms

* Remote VPN access was not working as expected.
* The router was operating behind the ISP modem.
* The upstream modem/router configuration created an additional NAT layer that interfered with inbound VPN connectivity.

## Troubleshooting

* Verified the local network and router were operating normally.
* Reviewed the WAN addressing and identified a double-NAT condition.
* Verified the DDNS configuration used for remote access.
* Configured No-IP DDNS so the VPN endpoint could be reached by hostname.
* Changed the ISP modem to bridge mode so the downstream router could receive the public WAN connection directly.
* Re-tested OpenVPN from an external connection.

## Root Cause

The VPN router was behind an additional NAT layer created by the ISP modem, preventing the remote-access path from working correctly.

## Solution

Placed the ISP modem in bridge mode, kept DDNS configured for the changing public IP, and re-tested OpenVPN successfully from outside the local network.

## Lessons Learned

* Remote-access VPN troubleshooting should include checking whether the router actually holds the public WAN IP.
* Double NAT can break or complicate inbound VPN connectivity.
* DDNS solves changing public-IP reachability, but it does not solve NAT or port-path problems by itself.
* Always test remote access from a truly external network after making changes.
