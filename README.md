# ThinkPad T440p Mojave OpenCore 1.0.7 Configuration

<img src="https://img.shields.io/badge/OpenCore-1.0.7-success" alt="OpenCore Version"> <img src="https://img.shields.io/badge/macOS-Mojave%2010.14-blue" alt="macOS Version"> <img src="https://img.shields.io/badge/Model-ThinkPad%20T440p-orange" alt="ThinkPad Model">

## Overview

This repository contains a fully functional OpenCore 1.0.7 configuration that enables macOS Mojave to run on the ThinkPad T440p.
This is a Hackintosh project designed for lazy people who can't be bothered to create their own EFI.

Remember to add your Serial Number, ROM (MAC address of ethernet card), UUID and MLB in config.plist/PlatformInfo/Generic

---

## Known Issues & Limitations

- **WiFi**: Airdropitlwm required disabling SIP and installing into /System/Extensions (Intel AC7260);
- **Discrete GPU**: T440p models with Nvidia dGPU will encounter limitations (Haswell Nvidia cards not supported in Mojave)
- **DisplayPort**: not tested

---

## Performance Notes

- **Battery Life**: 3-4 hours typical usage (80% battery health) - about the same as my Void install with undervolting
- **Boot Time**: ~40 seconds to desktop on SSHD (HFS+)
- **Temperature**: GETS HOT on load!!! (i7-4800MQ)
- **Real-World Use**: Suitable for daily driver usage

---

## Updating OpenCore

To update from a previous OpenCore version:

1. Download the latest OpenCore release
2. Extract and copy the new files to your EFI partition
3. Compare your current `config.plist` with the new sample configuration
4. Update configuration values carefully using a plist editor
5. Rebuild kext cache if needed
6. Test boot process

---

## Support & Issues

For issues specific to this configuration:

1. Check the "Known Issues" section above
2. Review the Troubleshooting guide
3. Search existing GitHub issues
4. Create a new issue with detailed information including:
   - Exact hardware configuration
   - Detailed error messages or panic logs
   - Steps taken before the issue occurred
   - OpenCore and kext versions in use
   
I might help you

---

## Credits

- **OpenCore Team**: For the outstanding bootloader
- **Acidanthera**: For kexts including Lilu, VirtualSMC, WhateverGreen, and AppleALC
- **OpenIntelWireless**: For itlwm kext and work on porting Intel BSD drivers to macOS
- **dhinakg**: For USBToolBox kext
- **averycblack**: For ECEnabler kext
- **Community Contributors**: For extensive documentation and testing
- **Apple**: For creating macOS, a really underappreciated OS (POLSKA NIE GOTOWA)

---

## License

This project is provided as-is for educational and personal use. Please respect intellectual property rights and use responsibly.