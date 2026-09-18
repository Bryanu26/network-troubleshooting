# DisplayPort Handshake Preventing BIOS Display

## Environment

HP Omen desktop connected to a monitor using DisplayPort.

## Symptoms

* No BIOS or POST screen was displayed.
* The monitor occasionally showed a noisy or corrupted image during startup.
* Windows would eventually display normally after booting.
* Entering the BIOS was not possible because no image was shown before Windows loaded.

## Troubleshooting

* Verified the monitor and DisplayPort cable.
* Tested different DisplayPort connections.
* Confirmed the system was powering on correctly.
* Tested an alternate display connection.
* Determined the issue was related to the DisplayPort initialization during POST.

## Root Cause

A DisplayPort handshake issue between the graphics card and the monitor prevented video output during the POST and BIOS stages.

## Solution

Used an alternate display connection/adapter to access the BIOS and restore normal startup video behavior.

## Lessons Learned

* No BIOS image does not always indicate a motherboard or GPU failure.
* DisplayPort handshake issues can occur before the operating system loads.
* Always test another cable, monitor, adapter, or display interface before replacing hardware.
