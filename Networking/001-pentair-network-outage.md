# Pentair Device Causing DHCP / Network Outage

## Environment

Residential network with UniFi equipment and Pentair pool controller.

## Symptoms

* Network instability.
* Clients experienced connectivity issues.
* Devices were unable to communicate reliably.

## Troubleshooting

* Verified router and switch operation.
* Checked physical connections.
* Isolated network devices one at a time.
* Disconnected the Pentair controller from the wired network.
* Monitored the network after each change.

## Root Cause

The Pentair controller was causing network instability when connected to the wired network, affecting normal DHCP and client communication.

## Solution

Disconnected the Pentair controller from the wired connection, restoring normal network operation. The issue was isolated to the Pentair device/path and further investigation was recommended before reconnecting it.

## Lessons Learned

* Isolate devices one by one when troubleshooting intermittent network issues.
* Third-party IoT devices can create unexpected network problems.
* Never assume the router or switch is at fault before eliminating endpoint devices.
