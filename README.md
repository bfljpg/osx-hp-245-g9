# OpenCore EFI for the HP 245 G9

:information_source: **The current version of the EFI is only compatible with macOS Ventura! Any other versions are UNTESTED!**

<br>

[![OpenCore](https://img.shields.io/badge/OpenCore-0.9.8-lightblue.svg)](https://github.com/acidanthera/OpenCorePkg)

:warning: **DISCLAIMER:**
THIS IS NOT A GUIDE!
\
\
This is simply an EFI backup for the HP 245 G9. Only use this EFI if you have the exact same model.
\
\
:warning: - **You are warned hereby that we are not responsible for bricked computers, dead GPUs, your CPU turning into a nuclear power generator, or you getting fired because Clock.app failed. Please do some research if you have any concerns about the stability of Hackintosh. YOU are choosing to install this unsupported OS on your computer, and if you point the finger at us for messing up your device, we will laugh at you.**
<br>

## :computer: Hardware:

| **Category** | **Component**                                                                    |
| ------------ | -------------------------------------------------------------------------------- |
| **CPU**      | AMD Ryzen 5 5625U 6-Core Processor                                               |
| **GPU**      | AMD Radeon RX Vega 7                                                             |
| **RAM**      | 16GB DDR4 3200MHz                                                                |
| **SSD**      | WD Blue SN580 / SN770 Black                                                      |
| **Wi-Fi/BT** | Intel AX200 Wi-Fi 6 (default is RTL8852BE, unsupported)						  |
| **Ethernet** | Realtek RTL8111                                                                  |
| **Audio**    | Realtek ALC236 (layout-id=69)                                                    |

## :white_check_mark: Working:
- [x] CPU power management (still problematic due to AMD, but works fine)
- [x] Graphics acceleration (OpenGL acceleration seems to be working)
- [x] Keyboard & Trackpad
- [x] Wi-Fi
- [x] Bluetooth
- [x] USB ports
- [x] HDMI video & audio output
- [x] Ethernet (has issues due to the use of RTL8111.kext)
- [x] Audio (internal speakers, 3.5mm headphone jack)
- [x] Internal microphone
- [x] HP TrueVision Webcam
- [x] iCloud & App Store
- [x] iMessage & FaceTime

## :question: In-between:
- [x] AirDrop & Handoff - Works one-way from your iPhone to your "Mac", cannot work the other way due to itlwm limitations.

## :no_entry_sign: Not working:
- [x] Virtualization (due to the lack of AMD-V support in macOS)

## :closed_lock_with_key: SMBIOS

You will need to generate your own SMBIOS and edit the config, since it is required to boot macOS **at all**. 
The HP 245 G9 works best with the MacBookPro16,3 SMBIOS, but if a different one that works better is discovered, we'll update the repo.
Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate your own PlatformInfo values and then copy them to the related path in:

- Config.plist -> PlatformInfo -> Generic

## BIOS setup:

- Disable TPM and set the assigned VRAM to 1G at minimum, 2G is recommended. 
- Secure boot should also be off.

## Credits:

[**Acidanthera**](https://github.com/acidanthera) for [OpenCore](https://github.com/acidanthera/OpenCorePkg)

[**Dortania**](https://dortania.github.io/getting-started/) for their guide

[**CorpNewt**](https://github.com/corpnewt) for [ProperTree](https://github.com/corpnewt/ProperTree) and [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)

[**AMD-OSX**](https://github.com/AMD-OSX/AMD_Vanilla) for AMD Kernel Patches

[**Apple**](http://apple.com/) for obvious reasons
