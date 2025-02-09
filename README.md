# HP Envy13-AQ0026TU Hackintosh
This repository and project hosts the files necessary to boot macOS Ventura successfully on the HP Envy13-AQ0026TU Laptop

# DISCLAIMER
THIS INFORMATION/RESEARCH HAS BEEN DONE AND SHARED PURELY FOR EXPERIMENTAL AND RESEARCH PURPOSES, AND IS IN NO MAY MEANT TO PROMOTE CIRCUMVENTING OF ANYTHING THAT IS SOMEONE ELSE'S CORPORATE PRIVATE PROPERTY. THE INFORMATION LISTED HERE IS PURELY FOR EDUCATIONAL PURPOSES AND SHOULD YOU CHOOSE TO UTILIZE IT IN ANY WAY, I AM IN NO WAY RESPONSIBLE FOR ANY INJUNCTIONS/PROBLEMS THAT MAY OR MAY NOT ARISE AND/OR BE BROUGHT AGAINST ANOTHER FOR THEIR CHOOSING TO HAVE DONE SO.

# Acknowledgements
- Acidanthera for [OpenCore Bootloader](https://github.com/acidanthera/OpenCorePkg)
- Dortania for [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide)
- Corpnewt for [SSDT Time](https://github.com/corpnewt/SSDTTime)
- USBToolbox for [USBToolbox](https://github.com/USBToolBox)
- And many more awesome people in the hackintosh community
  
# Deployment
To deploy this project properly, please obtain the EFI folder from this repository, edit the config.plist to generate new serial number, rom, UUID, etcetera, then save config.plist, and place the files onto the appropriate ESP EFI partition in order to boot using OpenCore bootloader and proceed with your installation of macOS.

# Hardware
_The hardware in this Machine is as follows_:
- CPU: Intel Core i5-8265U (Whiskey Lake)
- GPU: Intel UHD Graphics 620
- Mobo: HP 85E2 (Intel 300 Series Chipset)
- Memory: 2x4GB DDR4 2400MHz (Samsung M378A5244CB0-CRC)
- Drive: LITEON CA3-8D256-HP
- Keyboard & Touchpad: PS2 Keyboard & I2C Synaptics Touchpad
- Wifi & Bluetooth: Intel Wireless-AC 9560 160MHz
- Audio: Realtek ALC285
- Microphone: Intel SST
- Camera: HP Wide Vision HD Camera
- SD Card Reader: BayHubTech Intergrated SD controller (SDA Compliant Host)
- Fingerprint Sensor: Synaptics WBDI SGX

# Drivers & Essential Kernel Extensions
| Required Drivers |
| ------------- |
| [HfsPlus.efi](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi) |
| [OpenRuntime.efi](https://github.com/acidanthera/OpenCorePkg) |

| Essential Kexts |
| ------------- |
| [Lilu.kext](https://github.com/acidanthera/Lilu) |
| [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC) |

# Kernel Extensions corresponding to hardware
| Hardware  | Kext(s) |
| ------------- | ------------- |
| Intel UHD Graphics 620  | [Whatevergreen.kext](https://github.com/acidanthera/WhateverGreen)  |
| PS2 Keyboard  | [VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2)  |
| I2C Synaptic Touchpad | [VoodooI2C.kext and its satellite VoodooI2CHID.kext](https://github.com/VoodooI2C/VoodooI2C)  |
| Intel 9560 Wifi | [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm)|
| Intel 9560 Bluetooth | [IntelBluetoothFirmware.kext; IntelBTPatcher.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) & [BlueToolFixup.kext](https://github.com/acidanthera/BrcmPatchRAM)|
| Realtek ALC285  | [AppleALC.kext](https://github.com/acidanthera/AppleALC) with layout-id 66  |
| Camera  | [USBToolBox.kext](https://github.com/USBToolBox/kext) & [UTBMap.kext](https://github.com/USBToolBox/tool)  |
| Brightness Key (Fn + F2/F3)  | [BrightnessKeys.kext](https://github.com/acidanthera/BrightnessKeys)  |

# Result
_Working_:
- iGPU
- Internal Sound
- Wifi & Bluetooth
- Keyboard
- Touchpad
- USB ports
- Brightness Keys
- Battery Status
- Camera

_Not working_:
- Microphone (Intel SST)
- Airdrop (Intel Wireless)
- Fingerprint Sensor
- SD Card Reader

# BIOS Settings
- **Security**
  - Intel Software Guard Extensions (SGX) ~> Disabled
  - TPM Device ~> Available
  - TPM State ~> Disabled
- **Configuration**
  - Virtualization Technology ~> Enabled
- **Boot Options**
  - Network Boot ~> Disabled
  - Legacy Support ~> Disabled
  - Secure Boot ~> Disabled
