# HDMI Balun Transmitting Video but No Audio

## Environment

Residential AV system using an HDMI-over-Cat6 balun with IR support.

## Symptoms

* Video displayed correctly on the TV.
* No audio was present.
* HDMI link appeared to be established successfully.

## Troubleshooting

* Verified HDMI cable connections.
* Confirmed the balun transmitter and receiver were connected correctly.
* Tested different HDMI inputs on the TV.
* Disabled and re-enabled HDMI-CEC.
* Disabled and re-enabled HDMI Plus (Enhanced HDMI).
* Re-established the HDMI connection after changing TV settings.

## Root Cause

The issue was caused by an HDMI handshake/negotiation problem between the source device and the TV, related to the TV's HDMI-CEC and HDMI Plus settings.

## Solution

Reset the TV's HDMI settings by disabling and re-enabling HDMI-CEC and HDMI Plus. After renegotiating the HDMI connection, audio was restored without replacing any hardware.

## Lessons Learned

* Video without audio does not always indicate a faulty balun.
* Verify HDMI handshake and TV settings before replacing equipment.
* HDMI-CEC and enhanced HDMI features can affect audio negotiation between devices.
