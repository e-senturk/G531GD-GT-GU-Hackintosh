# G531GT-Hackintosh
OpenCore Build for G531-GT

## V 1.0 Changelog:
- Working Sound(thanks to @ayatkyo for pinconfig)
- Working Trackpad(thanks to @serdeliuk)
- Working Intel UHD 630
- Working Sleep Wake Lid Close
- Support's DualBoot
- Replaced WifiCard and Bluetooth Support (DW1560)
- Fixed Unsupported NVME SSD( Can be enabled manually)
- Fixed Most Common Bugs(Power management etc.)

## Bugs:
- Trackpad Buttons not working.
- AsusSMC is not working in Catalina its a common bug. You cant use most fn keys and set backlight brightness. In keyboard
settings you can set fnbrightness keys for screen.
- Numberpad is not working (Probably it never will)
- You tell me.

## Installation:
- First read opencore installation docs for more info (https://github.com/acidanthera/OpenCorePkg). 
- Edit your device info (you might want to use OpenCore Configurator).
- If you want to install it only single drive install osx first then windows after all installation complete.
Copy efi folder to your drive and replace boot folder. Move windows folder into OC folder. Then use bless override
section and set windows boot file location. Disable hideself in misc.
- If you have two seperate drives install with oses in any order.Copy Efi folder into OSX drive.And enable hideself in misc.


## Q.A:
- Q-) My bios left on black screen what can I do? 
- A-) It's common bug after catalina for avoiding disable fast bios and use opencore for booting. 
Easy fix: Just select reset NVRam option in opencore

- Q-) I am getting kernel panic it says ionvme error what can I do?
- A-) Your nvme ssd is most likely not supported by apple you need to replace it or buy a sata ssd and enable SSDT_NVMe-Pcc.aml in config.plist

- Q-) I have bug kp error what can I do? 
- A-) Attach a debug and detailed information about bug. Without information I can't fix
anything.



