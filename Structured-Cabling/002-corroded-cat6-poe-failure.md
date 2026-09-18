# Corroded Cat6 Connection Causing PoE Failure

## Environment

Low-voltage network cabling carrying Ethernet and Power over Ethernet to a field device.

## Symptoms

* The endpoint was not operating normally.
* PoE delivery and network connectivity were unreliable or unavailable.
* The failure appeared to be localized to the cable path rather than the upstream network.

## Troubleshooting

* Verified the upstream network equipment was operating.
* Inspected the cable path and termination rather than assuming the powered device had failed.
* Identified corrosion on the Cat6 connection.
* Reworked/replaced the affected connection.
* Re-tested both network connectivity and PoE delivery after repair.

## Root Cause

Corrosion on the Cat6 connection degraded the physical link and interfered with reliable Ethernet/PoE operation.

## Solution

Corrected the damaged/corroded connection and verified that the endpoint regained normal network and power operation.

## Lessons Learned

* Physical-layer faults can present as device, switch, or configuration problems.
* PoE troubleshooting should include inspecting connectors and terminations for moisture or corrosion.
* Verify Layer 1 before replacing powered endpoints or network hardware.
