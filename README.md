# G531GT-Hackintosh
- G531-GT Hackintosh Build
# Please don't forget to type in terminal: sudo kextcache -i / command after installation. 
# Please don't forget to disable boot logo sound otherwise your speaker won't work.
## Working:
- OpenCore and Clover configuration
- Working Sound(thanks to @ayatkyo for pinconfig)
- Working Trackpad(thanks to @serdeliuk)
- Working Intel UHD 630
- Working Sleep Wake Lid Close
- Support's DualBoot in OpenCore and Clover
- Can be disabled unsupported NVME SSD - Micron 2200V:(https://github.com/acidanthera/bugtracker/issues/732)

## Bugs:
- No Nvidia 1650 and No HDMI (Can't be fixed)
- Trackpad Buttons not working. (No fix for that yet)
- No support for Intel Wi-Fi. For now need to replace WifiCard DW1820A isrecommended.
- AsusSMC is not working in Catalina its a common bug. You cant use most fn keys and set backlight brightness. In keyboard
settings you can set fnbrightness keys for screen. It has to work with mojave didn't tested.
- Numberpad is not working (Probably it never will)
- You tell me.

## Installation:
Clover
- Use clover folder on release.
- Edit your device info (you might want to use Clover Configurator).


OpenCore
- First read opencore installation docs for more info (https://github.com/acidanthera/OpenCorePkg). 
- Edit your device info (you might want to use OpenCore Configurator).
- If you want to install it only single drive install osx first then windows after all installation complete.
Copy efi folder to your drive and replace boot folder. Move windows folder into OC folder. Then use bless override
section and set windows boot file location. Disable hideself in misc.
- If you have two seperate drives install with oses in any order.Copy Efi folder into OSX drive. And enable hideself in misc.
- If trackpad or sound is not working rebuild cache with  sudo kextcache -i / command.

## Q.A:
- Q-) My bios left on black screen what can I do? 
- A-) It's common bug after catalina for avoiding disable fast bios and use opencore for booting. 
Easy fix: Just select reset NVRam option in opencore and use clover instead.

- Q-) My speaker is not working  what can I do? 
- A-) Please don't forget to disable boot logo sound otherwise your speaker won't work.

- Q-) I am getting kernel panic it says ionvme error what can I do?
- A-) Your nvme ssd is most likely not supported by apple you need to replace it or buy a sata ssd and enable SSDT_NVMe-Pcc.aml in config.plist

- Q-) I have bug kp error what can I do? 
- A-) Attach a debug and detailed information about bug. Without information I can't fix
anything.



