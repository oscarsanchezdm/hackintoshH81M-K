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

### What does work
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

## Working on
- **Hibernation** To enable hibernation, ``hibernatemode`` [must be set](https://www.lifewire.com/change-mac-sleep-settings-2260804) to 3 in ``pmset`` (25 will disable sleep, hibernating the computer every time). To do so, simply type ``sudo pmset -a hibernatemode 3`` in the console. However, the computer never wakes from sleep to hibernate. The reason could be because RTC S4-wakes [are blocked from ACPI](https://github.com/oscarsanchezdm/hackintoshH81M-K/blob/main/EFI/OC/ACPI/SSDT-GPRW.aml).

### BIOS Configuration
- Enable MultiMonitor support
- SATA in AHCI mode
- Disable CFG lock

### Credits
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/config.plist/haswell.html)
- [acidanthera](https://github.com/acidanthera/) for OpenCore, Lilu, WhateverGreen... and all the contributors
- [Mieze](https://github.com/Mieze/) for [Realtek Ethernet kext](https://github.com/Mieze/RTL8111_driver_for_OS_X)
- [corpnewt](https://github.com/corpnewt/) for [CPUFriendFriend](https://github.com/corpnewt/CPUFriendFriend)
- [hieplpvip](https://github.com/hieplpvip/) for  [SidecarEnabler](https://github.com/hieplpvip/SidecarEnabler)
- Apple for macOS
