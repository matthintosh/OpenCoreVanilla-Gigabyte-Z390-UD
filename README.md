# OpenCore Vanilla Hackintosh for Gigabyte Z390 UD - intel i5 9400F

## Works on config
- Intel i5 9400F (9gen Coffee lake)
- 16Go DDR4 2666Mhz
- AMD RX560 4Go (Asus Strix)
- macOS Catalina 10.15

## Infos

Please use GenSMBIOS for your hackintosh serial number and insert it in the config.plist file
The hack is using iMac19,1 (The i5 9400F CPU does not have iGPU)

## Debug

By default, the hackintosh will boot in verbose mode (necessary for macOs install).
You can change this parameter in the boot arguments (config.plist file).

## Kexts

- AppleALC
- Lilu
- RealtekRTL8111
- SMCProcessor
- SMCSuperIO
- USBInjectAll
- VirtualSMC
- WhateverGreen

## Tools

- Shell.efi (Z390 Motherboard has issues KALSR slide values)

## Bios

Version 10F

### Disable:
- Fast Boot
- VT-d(can be enabled if you set DisableIoMapper to YES, AMD users will need to disable SVM in the BIOS)
- CSM
- Thunderbolt
- Intel Platform Trust

### Enable:
- VT-x
- Above 4G decoding (depends if you have the KALSR issue)
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode

## OpenCore version
0.5.5
