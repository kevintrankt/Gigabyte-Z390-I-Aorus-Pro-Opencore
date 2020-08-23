# Gigabyte-Z390-I-Aorus-Pro-Opencore

This is my Opencore setup for the Gigabyte Z390 I Aorus Pro ITX motherboard. **This should be used as a reference**; there is no guarantee that my set up will work for yours even if you have the same hardware. This was originally a Clover build, but I converted to Opencore because I was tired of having to update so many things for each macOS update with Clover.

Currently using prebuilt SSDTs. I plan on compiling my own when I have the time.

## Hardware
* **CPU:** Intel Core i7-8700 3.2 GHz 6-Core Processor
* **GPU:** Sapphire Radeon RX 5700 XT 8 GB NITRO+ Video Card
* **RAM:** Corsair Vengeance LPX 32 GB (2 x 16 GB) DDR4-2666 CL16 Memory
* **Motherboard:** Gigabyte Z390 I AORUS PRO WIFI Mini ITX LGA1151 Motherboard
* **Audio Codec:** Realtek ALC1220
* **Ethernet:** Intel® i219v GbE LAN
* **Wifi/BT Card:** BCM94360CS2 + Airport to NGFF M.2 Adapter
* **BIOS revision:** F8c

## Software
* Opencore 0.6.0 RELEASE
* macOS 1.15.6 Catalina

## Kexts
* AppleALC - 1.5.1-RELEASE
* IntelMausi - 1.0.3-RELEASE
* Lilu - 1.4.6-RELEASE
* SMCProcessor - 1.1.5
* SMCSuperIO - 1.1.5
* VirtualSMC - 1.1.5-RELEASE 
* WhateverGreen - 1.4.1-RELEASE

## What Works
* WiFi + Bluetooth
* iMessage + Facetime
* Airdrop
* Sidecar
* Handoff
* Continuity
* Sleep
* Pretty much everything I've tested works.

### Process
1. Follow [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) for Coffee Lake builds.
2. Ensure `AppleXcpmCfgLock` and `AppleCpuPmCfgLock` are enabled under `Kernel -> Quirks` in order for Opencore to boot into your installation media.
3. Follow [this doc ](https://dortania.github.io/OpenCore-Post-Install/universal/security.html) to enable FileVault. `AuthRestart`, `UIScale`, `HashServices`, and `ExitBootServicesDelay` unchanged.
