# Introduction

My personal EFI configuration (OpenCore version 1.0.3) for Lenovo G50-80. Running latest macOS sequoia (15.3.1 at time of writing) with help of OCLP rootpatches. Made from scratch using dortania's opencore guide.

# Specifications

Model: Lenovo G50-80 80E5

CPU: Intel Core i5 5200U

GPU: Intel HD Graphics 5500

RAM: SKhynix 4GB + 8GB DDR3L @ 1600mhz

Audio: Conexant CX20751

Touchpad: Elan PS/2 

Disk: Crucial MX500 SSD 512GB + WD Blue HDD 1TB (on caddy)

Ethernet: Realtek RTL8111/8168/8411 PCI Express Gigabit Ethernet

Wi-Fi + Bluetooth: Intel AC Wireless 3160

Webcam: Lenovo EasyCamera 720p 

SD Card Reader: Realtek SD Card Reader

# Current Status

1. Hardware Video Decoding: Fully working
2. Audio: Fully working
3. Webcam: Fully working
4. SD Card Reader: Reader gets detected, SD card doesn't. WIP.
5. Ethernet: Should work, not tested.
6. Battery Reporting: Working properly with slight inaccuracy.
7. USB: Fully working, properly mapped.
8. Wi-Fi: Fully working if used with itlwm. Requires spoofing and root patching if using AirportItlwm.
9. Bluetooth: Fully working
10. Touchpad: Fully working
11. Hardware DRM: Broken, not fixable on iGPU only systems.
12. Sleep and Hibernation: Fully working, even the sleep to hibernation logic. 


Note 1: macOS Ventura+ requires root patching for our specific GPU to support Hardware Acceleration.

Note 2: Since I have unlocked the bios on my own model, I do not need to use many "hacks" which would be required otherwise.

# BIOS Settings

Fast Boot: Can be left on.
Virtualization: ON
Secure Boot: OFF


Settings which I would recommend if you have unlocked bios:

In Advanced > Chipset Configuration: 
RTC Lock: OFF,
Board Capability: DeepSx,
DeepSx Power Policies: Enable S3-S4-S5


Native ASPM: ON

