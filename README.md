# OpenCore EFI for the HP 245 G9

:information_source: **The current version of the EFI is only compatible with Ventura and below!**

<br/>

[![OpenCore](https://img.shields.io/badge/OpenCore-0.9.8-lightblue.svg)](https://github.com/acidanthera/OpenCorePkg)
[![macOS](https://img.shields.io/badge/macOS-14.3.1-F09337.svg)](https://www.apple.com/macos/ventura)

:warning: **DISCLAIMER:**
THIS IS NOT A GUIDE!
<br/>
It's just my complete EFI for my hardware based on my experiments, please refer to [Dortania](https://dortania.github.io/getting-started/) before doing anything. I am not responsible for any damage. This OpenCore configuration is optimized for my specific hardware, so please use it only as a reference or if you happen to have the same or similar hardware.

## :computer: Hardware:

| **Category** | **Component**                                                                    |
| ------------ | -------------------------------------------------------------------------------- |
| **CPU**      | AMD Ryzen 5 5625U 6-Core Processor                                               |
| **GPU**      | AMD Radeon RX Vega 7                                                             |
| **RAM**      | 16GB DDR4 3200MHz                                                                |
| **SSD**      | Kingston SNV2 / SN770 Black                                                      |
| **Wi-Fi/BT** | Intel AC-8265 / AX200 (default is RTL8852BE)                                     |
| **Ethernet** | Realtek RTL8111                                                                  |
| **Audio**    | Realtek ALC236 (layout-id=69)                                                    |

## :white_check_mark: Working:

- [x] CPU power management
- [x] Graphics acceleration
- [x] Keyboard & Trackpad
- [x] Wi-Fi
- [x] Bluetooth
- [x] USB ports
- [x] HDMI video & audio output
- [x] Ethernet. (has issues due to the use of RTL8111.kext)
- [x] Audio (internal speakers, 3.5mm headphone jack)
- [x] Internal microphone
- [x] HP TrueVision Webcam
- [x] iCloud & App Store
- [x] iMessage & FaceTime

## :x: Untested:
- [x] AirDrop & Handoff


## :closed_lock_with_key: SMBIOS

You will need to generate your own SMBIOS and configure, since is required to fully work with macOS. As per this [guide](https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html#platforminfo) you can use the following SMBIOS: MacBookPro16,3. Note that if your hardware is different for the one mentioned [here](#computer-hardware) you have to choose an appropriate SMBIOS, more details in the [guide](https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html).

Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate your own unique SMBIOS and then copy each parametter following path (recomended to follow the guide above):

- Config.plist -> PlatformInfo -> Generic

## BIOS setup:

IMPORTANT: Disable TPM and set the assigned VRAM to 1G at minimum, 2G is recommended.

## Credits:

[**Gabriel Luchina**](https://luchina.com.br)

[**AMD-OSX**](https://github.com/AMD-OSX/AMD_Vanilla)

[**Acidanthera**](https://github.com/acidanthera)

[**Dortania**](https://dortania.github.io/getting-started/)

[**Apple**](http://apple.com/)
