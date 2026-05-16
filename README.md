[![](https://img.shields.io/badge/Gitter%20HL%20Community-Chat-informational?style=flat&logo=gitter&logoColor=white&color=ed1965)](https://gitter.im/Hackintosh-Life-IT/community)
[![](https://img.shields.io/badge/EFI-Release-informational?style=flat&logo=apple&logoColor=white&color=9debeb)](https://github.com/Speeedo83/Dell-Inspiron-5491-2in1-Hakintosh/releases)
[![](https://img.shields.io/badge/Telegram-HackintoshLifeIT-informational?style=flat&logo=telegram&logoColor=white&color=5fb659)](https://t.me/HackintoshLife_it)
[![](https://img.shields.io/badge/Facebook-HackintoshLifeIT-informational?style=flat&logo=facebook&logoColor=white&color=3a4dc9)](https://www.facebook.com/hackintoshlife/)
[![](https://img.shields.io/badge/Instagram-HackintoshLifeIT-informational?style=flat&logo=instagram&logoColor=white&color=8a178a)](https://www.instagram.com/hackintoshlife.it_official/)

# Asrock H510m HDV\M2 i5 10400 + Sapphire RX 580 4g

EFI for Dell Inspiron 5491 with OpenCore bootloader

(Compatible for Dell Inspiron 5491/5591, these laptops use the same bios file)

![descrizione](./Screenshot/pc.png)


### Computer Spec:

| Component        | Brank                              |
| ---------------- | ---------------------------------- |
| CPU              | Intel i7 10510U (4C-8T 8MB CML)    |
| iGPU             | Intel® Graphics Graphics UHD       |
| Audio            | Realtek ALC236                     |
| Ram              | 16 GB DDR4 2666 Mhz                |
| Wifi + Bluetooth | BCM94360NG Fenvi                   |
| NVMe             | HYNIX BC511 512 GB (MACOS)         |
| SSD Sata         | SPCC Silicon Power 1TB (WINDOWS)   |
| SmBios           | MacBookPro 16,3                    |
| BootLoader       | OpenCore 0.6.9                     |
| macOS            | Big Sur 11.3.1                     |



![infobigsur](./Screenshot/infomac.png)

### What works and What doesn't or WIP:

- [x] Intel Graphics UHD iGPU 
- [x] Intel Graphics UHD iGPU HDMI Output
- [x] IIntel Graphics UHD iGPU Type-C to HDMI Output
- [x] ALC236 Internal Speakers
- [ ] ALC236 Internal microphone (Digital Mic Intel SST not compatible)
- [x] USB MINI Dongle Microphones  *
- [x] ALC236 Combojack headphones
- [ ] ALC236 Combojack microphone (WIP)
- [x] ALC236 HDMI Audio Output
- [x] ALC236 TYPE-C to HDMI Audio Output
- [x] All USB-A 3.1 Ports (TYPE-C 3.2 Included)
- [x] SpeedStep / Sleep / Wake **
- [x] HID Key PWRB & SLPB 
- [x] I2C Touch pad with gesture
- [x] I2C Touch Screen
- [x] Keyboard (PS2-Internal) with backlight
- [x] F6 & F7 Brightness Key
- [x] F10 Print Screen Key
- [x] F1 & F2 & F3 Sound Key
- [x] Wi-Fi and Bluetooth BCM94360NG Module
- [x] Controller SATA III
- [x] Controller NVME PciE Gen3x4 
- [x] Micro SD Cardreader (USB-Internal)
- [x] WebCam (USB-Internal)
- [x] All Sensors CPU, IGPU, BATTERY, NVME, SATA, FAN
- [x] ACPI Battery
- [x] Apple VTD
- [x] NVRAM (Native)
- [x] Recovery (macOS) boot from OpenCore
- [x] Windows 10 boot from OpenCore

## OpenCore 0.6.9 Custum Gui by HachintoshLife

![GUIOC](./Screenshot/GUIOC.png)

## Trik Mic Fix
* USB Dongle Mic:
At the moment there is no fix for the internal microphone and combojack microphone, as both are managed by the SST (Smart Sound Technology Intel) drive.
I use a USB dongle and it works perfectly.


![usbdongle](./Screenshot/usbdongle.png)       ![usbmic](./Screenshot/usbmic.png)

## All Apple native shortcuts for sleep, log out and Shut Down

![stopawake](./Screenshot/stopawake.png)

##Performance Sleep

![sleep](./Screenshot/sleep.png)


## CPU Performance by CPU Friend settings

![cpufreq](./Screenshot/cpufreq.png)

See [CPUFriend](https://github.com/acidanthera/CPUFriend) For more info 


## Peripherals & TouchPad Setting & Benchmarks

![infohack](./Screenshot/periferiche.png)
![infopci](./Screenshot/pci-dev.png)
![touchpad](./Screenshot/touchpad.png)
![trascinamento](./Screenshot/trascinamento.png)
![finger](./Screenshot/finger.png)
![Temp-Fan-Control](./Screenshot/Temp-Fan-Control.png)
![speedtest](./Screenshot/speedtest.png)
![CPU](./Screenshot/CPU.png)
![metal](./Screenshot/metal.png)
![videoproc](./Screenshot/videoproc.png)
![test](./Screenshot/teststorage.png)


### Special Config:/Users/mario/Desktop/image

- Usb port mapping performed
- SSDT-Hack Essential patch
- Applied cosmetics PCI Dev

See [ioreg](https://github.com/Speeedo83/Dell-Inspiron-5491-2in1-Hakintosh/raw/main/ioregMacBookPro.zip) for more clarification


### MacOS bootable USB creation:
- Read the Dortania guide for creating your USB from Windows or macOS
- [Guide Dortania](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) - USB creation


## Bios settings
### Enable :
* SATA Operation : AHCI
* Fastboot : Thorough
* Integrated NIC : Enable


### Disable : 
* Secure Boot
* Absolute
* TPM2.0 Security On
* Intel SGX
* SMM Security Migration
* Wake on AC
* Wake on Dell USB-C Dock
* Power On Lid Open
* Enable UEFI Network Stack
* Sign Of Life : Early Logo Display / Early keyboard backlight
* cfg lock and DVMT: DO AT YOUR OWN RISK!!! It may brick your laptop.

## Guide

Create a usb in FAT with MBR map and put ru.efi in it then go to the bios, and create an entry with the path of the usb and setting the ru.efi file and the name of your choice startup and then send and finally click apply.
Restart and press f12 among the entries you will have the last created, click any key, then click alt + ì a menu will appear and scroll to CpuSetup and click enter, in the new screen go with the arrows on the value and change it from 01 to 00 and click enter and then ctrl + w to save and then alt + q to exit. proceed to check if your CFG LOCK is unlocked.
![CFG](./Screenshot/CFG.png)

For the 2 DVMT values you have to go to the SaSetup menu and enter.
Look The picture and set:
![DVTM](./Screenshot/DVTM.png)
save with ctrl + w and to exit alt + q and you will have the suitable DVMT values to the igpu


## Color profile icc with SpiderX Datacolor Pro (Standard ambient light) Screen brightness 80% 
See [calibrazione](https://github.com/Speeedo83/Dell-Inspiron-5491-2in1-Hakintosh/blob/main/Dell%20Inspire5491.icc)
 

## Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html) For great and detailed guides.
- [Lorys89](https://github.com/Lorys89/) for making this hack perfect. 
- [Hackintoshlifeit](https://github.com/Hackintoshlifeit) Support group for installation and post installation.

# If you need help please contact us on [Telegram](https://t.me/HackintoshLife_it) or [Web](https://www.hackintoshlife.it/)
