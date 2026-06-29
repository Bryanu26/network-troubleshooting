# UniFi Access Point Adoption Failure

## Environment

Residential network using UniFi infrastructure.

## Symptoms

* Access Point appeared in the UniFi Controller.
* Device remained in a pending or failed adoption state.
* AP did not become manageable through the controller.

## Troubleshooting

* Verified PoE power to the AP.
* Confirmed network connectivity.
* Checked DHCP assignment.
* Verified the controller could reach the AP.
* Performed a factory reset by holding the reset button for 10+ seconds.
* Re-attempted adoption through the UniFi Controller.
* Verified firmware after successful adoption.

## Root Cause

The Access Point had not been properly factory reset, preventing it from completing the adoption process.

## Solution

Performed a complete factory reset and adopted the AP again through the UniFi Controller. Once adopted, updated the firmware and verified normal operation.

## Lessons Learned

* Always perform a full factory reset before troubleshooting adoption issues.
* Verify power and DHCP before assuming a controller problem.
* Keep firmware updated after a successful adoption to avoid compatibility issues.
