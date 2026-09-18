# Pool Controller Wi-Fi Security Compatibility Issue

## Environment

Residential wireless network with a pool automation controller.

## Symptoms

* The pool controller would not connect to the wireless network.
* The SSID and password were correct.
* Other wireless clients were able to use the network normally.

## Troubleshooting

* Verified the wireless SSID and password.
* Confirmed the Wi-Fi network itself was operational.
* Reviewed the wireless security settings used by the SSID.
* Identified a compatibility issue between the pool controller and the configured Wi-Fi security/encryption mode.
* Changed the SSID security setting to a WPA2-compatible configuration.
* Reconnected the pool controller and verified that it joined the network successfully.

## Root Cause

The pool controller was not compatible with the wireless security/encryption mode configured on the SSID.

## Solution

Adjusted the Wi-Fi security configuration to WPA2 compatibility and reconnected the controller. The device then joined the wireless network successfully.

## Lessons Learned

* Correct credentials do not guarantee that an IoT device supports the security mode used by the SSID.
* Older or embedded devices may fail on WPA2/WPA3 mixed or newer security configurations.
* When an IoT device can see an SSID but cannot join it, check security compatibility before assuming a signal, DHCP, or password problem.
