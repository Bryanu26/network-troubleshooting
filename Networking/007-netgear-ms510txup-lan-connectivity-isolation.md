# Netgear MS510TXUP - LAN Connectivity Isolation

## Environment

Network using a Netgear MS510TXUP switch and a router with a recently changed LAN subnet.

## Symptoms

* The router and switch were reachable by ping.
* Wi-Fi connectivity was working.
* Wired LAN clients did not have normal Internet access.
* Multiple resets and DHCP renew attempts did not immediately resolve the issue.

## Troubleshooting

* Factory-reset the affected network equipment during isolation.
* Released and renewed the client DHCP lease.
* Verified the LAN subnet and subnet mask after the router addressing change.
* Tested alternate DNS servers to rule out a DNS-only failure.
* Confirmed that the router could still be reached by ping.
* Changed switch/router ports and replaced the patch cable.
* Re-tested wired connectivity after each physical change.

## Root Cause

The issue was isolated to the physical wired path, with the port or patch cable being the likely failure point rather than DHCP, DNS, or the router configuration.

## Solution

Moved the connection to a different port and changed the patch cable, restoring normal wired connectivity.

## Lessons Learned

* A successful ping to the gateway does not guarantee that the full wired path is healthy.
* Do not stay at Layer 3 too long when Wi-Fi works but one wired path does not.
* Swap known-good cables and ports early when symptoms point to a localized LAN issue.
* Use configuration changes only after basic physical-path checks have been completed.
