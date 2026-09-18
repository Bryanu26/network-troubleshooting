# UniFi WAN Migration - SFP vs Copper Recovery

## Environment

Residential network using a UniFi gateway with both copper Ethernet and SFP WAN interface options.

## Symptoms

* Internet connectivity was lost after a WAN interface migration.
* The network gateway remained powered and local infrastructure was still present.
* The issue appeared immediately after changing the active WAN interface from copper to SFP.

## Troubleshooting

* Reviewed the recent WAN interface change as the most likely source of the outage.
* Verified the physical uplink path and interface assignment.
* Confirmed that the SFP-based WAN configuration was not operating as expected.
* Restored the WAN connection to the previous copper Ethernet interface.
* Recovered the UniFi configuration using the available backup when needed.
* Verified that Internet connectivity and normal gateway operation returned after rollback.

## Root Cause

The WAN interface migration to SFP introduced a configuration/physical-media mismatch that prevented the gateway from maintaining normal upstream connectivity.

## Solution

Rolled the WAN connection back to the known-good copper interface, restored the working UniFi configuration, and verified full network recovery.

## Lessons Learned

* Treat WAN interface changes as production-impacting changes and always have a rollback plan.
* Verify physical media, transceiver compatibility, and interface assignment before migrating an uplink.
* When an outage begins immediately after a configuration change, validate or reverse that change before troubleshooting unrelated parts of the network.
* Backups significantly reduce recovery time when a gateway or management configuration becomes unstable.
