 **Note**: Please use this configuration as a base for your own configuration. I've made this to suit my own needs.

# Dell Inspiron 14 5459 OpenCore EFI 
OpenCore configuration, kernel extensions and ACPI patches for Dell Inspiron 14 5459 i7 variant.
![alt text](https://i.ibb.co/2gQ8kQc/A-nh-chu-p-Ma-n-hi-nh-2022-04-02-lu-c-14-55-49.png "macOS 12.2.1 Monterey on Dell Inspiron 14 5459")
#### Laptop Specifications:
* Intel® Core™ i7-6500U @ 2.50 GHz
* Intel® HD Graphics 520
* 4GB DDR3L 1600 MHz RAM
* 14-inch HD WLED Display
* Intel Dual Band Wireless AC 3160 Wi-Fi and Bluetooth
* 1 USB 3.0 port, 2 USB 2.0 port
* HDMI port
* SD card reader
#### BIOS Setup:
* Enable UEFI Network Stack: Off
* Enable Legacy Option ROMs: Off
* SATA Operation: AHCI
* Secure Boot Enable: Disabled
* Intel® SGX Enable: Disabled
* Multi Core Support: All
* Intel® TurboBoost™: Enabled
* Virtualisation: Enabled
#### Working features:
* macOS 12.2.1 Monterey
* Built-in keyboard (with function keys)
* Built-in trackpad (with gestures)
* HDMI Video and Audio
* Integrated Camera
* Ethernet
* Native audio with AppleALC, including headphones
* Battery status
* USB 3.0 and 2.0
* Sleep and Wake
#### To be fixed:
* USB mapping (the port works but I have not map it correctly)
* Microphone
* Power Management (battery drains a lot)

You could try fixing Wi-Fi and Bluetooth with [itlwm or Airportitlwm](https://github.com/OpenIntelWireless/itlwm/releases) since it is stated as compatible in [this compatibility list](https://openintelwireless.github.io/itlwm/Compat.html). But it does not work for me. It is recommended to buy another Wi-Fi card for better compatibility and features.

#### Credits
* [Acidanthera](https://github.com/acidanthera) for [OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg), [AppleALC](https://github.com/acidanthera/AppleALC), [BrightnessKeys](https://github.com/acidanthera/BrightnessKeys), [CPUFriend](https://github.com/acidanthera/CPUFriend), [Lilu](https://github.com/acidanthera/Lilu), [WhateverGreen](https://github.com/acidanthera/WhateverGreen), [VirtualSMC](https://github.com/acidanthera/VirtualSMC) 
* [CorpNewt](https://github.com/corpnewt) for [USBMap](https://github.com/corpnewt/USBMap), [SSDTTime](https://github.com/corpnewt/SSDTTime)
* [Mieze](https://github.com/Mieze) for [RealtekRTL8100](https://www.insanelymac.com/forum/files/file/259-realtekrtl8100-binary/)
* [RehabMan](https://github.com/RehabMan) for [USBInjectAll](https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/)
* [Dortania](https://github.com/dortania) for [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
* And all of the people from [/r/Hackintosh Paradise Discord server](https://discord.gg/u8V7N5C) that helped me configuring my laptop
