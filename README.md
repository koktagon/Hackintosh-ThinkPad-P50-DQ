# Hackintosh Lenovo ThinkPad P50
## macOS Ventura 13.7 - OpenCore 1.0.2 - Intel Core i7-6820HQ - Deutsche Qualität

Things that are working and their corresponding kexts:
- Intel HD 530 Graphics - [WhateverGreen](https://github.com/acidanthera/WhateverGreen)
- Realtek Audio - [AppleALC](https://github.com/acidanthera/AppleALC), layout ID 29 
- Intel AC 8260 WiFi+BT - [AirportItlwm](https://github.com/OpenIntelWireless/itlwm) + [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) 
- Intel Ethernet - [IntelMausi](https://github.com/acidanthera/IntelMausi)
- USB
- Built-in keyboard and TrackPoint - [VoodooPS2](https://github.com/acidanthera/VoodooPS2)
- Built-in Synaptics UltraNav SMBus trackpad - [VoodooRMI](https://github.com/VoodooSMBus/VoodooRMI)
- Built-in Realtek SD card reader - [Sinetek-rtsx](https://github.com/cholonam/Sinetek-rtsx)

Untested:
- Video outputs (HDMI + Mini-DP)
- ExpressCard
- SmartCard

Not working:
- AirDrop + Handoff (use a real BCM94360NG card)
- Thunderbolt 3 (I didn't map the corresponding USB-C port to begin with since I have no use for it anyway)
- Nvidia Quadro M1000M/M2000M dGPU (The web driver hasn't been supported beyond High Sierra without OCLP root patches)

SMBIOS is blanked on purpose, you need to provide your own, use 
[GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) for that (use a MacBookPro14,3 SMBIOS)
