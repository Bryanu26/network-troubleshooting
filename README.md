# Network Troubleshooting Portfolio

This repo is a collection of real troubleshooting cases from field work, plus a few personal lab cases.

I work mostly with networking, Wi-Fi, fiber, structured cabling, AV, and access control. I use this repo to document what failed, how I tested it, what fixed it, and what I learned.

## Skills Demonstrated

- TCP/IP, DHCP, DNS, subnets, and gateway troubleshooting
- Wi-Fi troubleshooting, AP replacement, adoption, and migration
- WAN troubleshooting, NAT, DDNS, VPN, and rollback/recovery
- Switch port, VLAN, PoE, and physical-layer verification
- Fiber inspection, cleaning, and link troubleshooting
- Cat6/RJ45 troubleshooting and field cabling
- SSH and device management
- Relay logic and basic access-control integration
- Field documentation and cable mapping

## Tools & Platforms

UniFi · Ruckus · Netgear · OpenVPN · No-IP/DDNS · OvrC · WiFiman · SSH · PoE · Fiber · Cat6/RJ45

## Field Cases

### Networking

- [Pentair device causing network instability](Networking/001-pentair-network-outage.md)
- [UniFi AP adoption failure](Networking/002-unifi-ap-adoption-failure.md)
- [UniFi WAN SFP to copper recovery](Networking/005-unifi-wan-sfp-vs-copper-recovery.md)
- [OpenVPN, DDNS, double NAT, and modem bridge](Networking/006-openvpn-ddns-double-nat-and-modem-bridge.md)
- [Netgear MS510TXUP LAN connectivity isolation](Networking/007-netgear-ms510txup-lan-connectivity-isolation.md)

### Wireless

- [Ruckus ZoneDirector failure and migration to Unleashed](Wireless/001-ruckus-zonedirector-failure-migration-to-unleashed.md)
- [Pool controller Wi-Fi security compatibility](Wireless/002-pool-controller-wifi-security-compatibility.md)
- [Offline APs: hardware failure and replacement](Wireless/003-offline-access-points-hardware-failure-and-replacement.md)

### Fiber Optics

- [Fiber link failure caused by a contaminated LC connector](Fiber-Optics/001-contaminated-lc-connector.md)
- [Intermittent fiber video loss](Fiber-Optics/002-intermittent-fiber-video-loss.md)

### Structured Cabling

- [Faulty RJ45 termination causing intermittent signal loss](Structured-Cabling/001-faulty-rj45-termination-hdmi-balun.md)
- [Corroded Cat6 connection causing PoE failure](Structured-Cabling/002-corroded-cat6-poe-failure.md)

### Access Control

- [DoorBird / Altronix NO-NC relay troubleshooting](Access-Control/001-doorbird-altronix-no-nc-trigger-troubleshooting.md)

### AV Systems

- [HDMI balun: video but no audio](AV-Systems/001-hdmi-balun-no-audio.md)
- [Smart TV unable to connect to Wi-Fi](AV-Systems/002-smart-tv-unable-to-connect-to-wifi.md)
- [Existing speaker cabling field mapping](AV-Systems/003-existing-speaker-cabling-field-mapping.md)

## Lab / Personal

- [Home network subnet conflict](Networking/003-home-network-subnet-conflict.md)

## Systems / Hardware

- [DisplayPort handshake preventing BIOS display](Systems/001-displayport-handshake-no-bios.md)
- [Failed drive preventing Windows boot](Systems/002-failed-hard-drive-preventing-windows-boot.md)

## How I Troubleshoot

I try to start with the simplest checks first: physical connection, power, IP address, gateway, and reachability. From there I narrow the problem down instead of changing multiple things at once.

Some of these cases include mistakes, failed attempts, or escalation to someone with more experience. I keep those details when they are useful because that is part of how I learned the fix.
