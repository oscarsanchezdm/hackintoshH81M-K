# macOS on ASUS H81M-K
OpenCore EFI folder for ASUS H81M-K motherboard.

Current version:
OpenCore 0.6.3 Release

Tested on:
- Intel Core i5 4460
- Gigabyte AMD RX 5600 XT
- macOS Big Sur 11.1

### How to install
Clone this repository and copy the EFI folder inside your EFI partition. You will need to use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate serial and UUID. I recommend using iMac15,1 as SMBIOS.

### What works
- Power Management
- Audio
- Sleep
- Ethernet
- GPU
- IGPU (you should enable it under BIOS)
- DRM support
- SideCar (there may be some glitches)
- OpenCanopy (press alt KEY to enter the menu)

### What does not work
- Boot Chime

### Not tested yet
- Hibernation

### BIOS Configuration
- Enable MultiMonitor support.
- SATA in AHCI mode.
- Disable CFG lock

### Credits
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/config.plist/haswell.html)
- [acidanthera](https://github.com/acidanthera/) for OpenCore, Lilu, WhateverGreen... and all the contributors
- [Mieze](https://github.com/Mieze/) for [Realtek Ethernet kext](https://github.com/Mieze/RTL8111_driver_for_OS_X)
- [corpnewt](https://github.com/corpnewt/) for [CPUFriendFriend](https://github.com/corpnewt/CPUFriendFriend)
- [hieplpvip](https://github.com/hieplpvip/) for  [SidecarEnabler](https://github.com/hieplpvip/SidecarEnabler)
- Apple for macOS
