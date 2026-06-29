# HDMI Signal Loss Caused by Faulty RJ45 Termination

## Environment

Residential AV system using an HDMI-over-Cat6 balun.

## Symptoms

* HDMI video would intermittently cut out.
* Moving the RJ45 connection on the TV-side balun caused the video signal to disconnect and reconnect.
* Audio issues had already been resolved, but the unstable video remained.

## Troubleshooting

* Verified HDMI cable connections.
* Observed that the issue only occurred when the RJ45 connector was moved.
* Inspected the Cat6 termination.
* Determined that the instability was isolated to the Ethernet connection between the balun and the cable.

## Root Cause

A poor or loose RJ45 termination caused intermittent signal loss between the HDMI balun and the Cat6 cable.

## Solution

Re-terminate or replace the RJ45 connector to ensure all conductors are properly seated and maintain a stable connection. Verify signal stability after re-termination.

## Lessons Learned

* Intermittent issues caused by physical movement often point to a bad cable termination.
* Always inspect and test cable terminations before replacing active equipment.
* A simple RJ45 termination issue can mimic a faulty HDMI balun.
