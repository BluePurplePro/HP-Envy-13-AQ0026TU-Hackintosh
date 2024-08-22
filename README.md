# HP Envy13-AQ0026TU Hackintosh
This repository and project hosts the files necessary to boot macOS Ventura successfully on the HP Envy13-AQ0026TU Laptop

# DISCLAIMER
THIS INFORMATION/RESEARCH HAS BEEN DONE AND SHARED PURELY FOR EXPERIMENTAL AND RESEARCH PURPOSES, AND IS IN NO MAY MEANT TO PROMOTE CIRCUMVENTING OF ANYTHING THAT IS SOMEONE ELSE'S CORPORATE PRIVATE PROPERTY. THE INFORMATION LISTED HERE IS PURELY FOR EDUCATIONAL PURPOSES AND SHOULD YOU CHOOSE TO UTILIZE IT IN ANY WAY, I AM IN NO WAY RESPONSIBLE FOR ANY INJUNCTIONS/PROBLEMS THAT MAY OR MAY NOT ARISE AND/OR BE BROUGHT AGAINST ANOTHER FOR THEIR CHOOSING TO HAVE DONE SO.

# Acknowledgements
- https://dortania.github.io/OpenCore-Install-Guide/
  
# Deployment
To deploy this project properly, please obtain the EFI folder from this repository, edit the config.plist to generate new serial number, rom, UUID, etcetera, then save config.plist, and place the files onto the appropriate ESP EFI partition in order to boot using OpenCore bootloader and proceed with your installation of macOS.

# Hardware
_The hardware in this Machine is as follows_:
- CPU: Intel Core i5-8265U (Whiskey Lake)
- GPU: Intel UHD Graphcis 620
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
- https://support.hp.com/us-en/document/c06358461

# Result
_Working_:
- iGPU
- Internal Sound
- Wifi & Bluetooth
- Keyboard
- Touchpad
- USB ports
- Brightness
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
