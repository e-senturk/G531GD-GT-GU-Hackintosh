# G531GD-GT-GU-Hackintosh
# Important Notes
## Select best configuration for your system and use that config file into EFI/OC folder -- Example: EFI/OC/config.plist
## Please don't forget to type in terminal: sudo kextcache -i / command after installation. It might be required for some drivers.
## Please don't forget to disable boot logo sound otherwise your speaker won't work.
## Please edit your PlatformInfo configuration with OpenCoreConfigurator.

# Apps to install for better experiance
## RogHID = Enables brightness and keyboard backlight keys.
    https://github.com/black-dragon74/ROG-HID
## RogSwitch = Menu bar keyboard backlight color controller
    https://github.com/black-dragon74/ROGSwitch
## macAura = Advanced keyboard backlight color controller
    https://github.com/serdeliuk/macAura
## HeliPort: Intel Wireless App use it only with iwlwm config
    https://github.com/OpenIntelWireless/HeliPort

## Features:
- Supports Mojave, Catalina and BigSur
- Only OpenCore Configuration
- Supports both Intel 9560 wifi and Broadcom DW1820A wifi cards
- Working Sound(thanks to @ayatkyo for pinconfig)
- Nvidia GPU can be disabled and re-enabled with VirtualBiosMods for better battery.(thanks to @serdeliuk)
- Working Trackpad(thanks to @serdeliuk)
- Working Intel UHD 630
- Working Sleep Wake Lid Close
- Support's OsX, Windows and Linux
- Can be disabled unsupported NVME SSD - Micron 2200V:(https://github.com/acidanthera/bugtracker/issues/732)

## Bugs:
- No Nvidia 1650 and No HDMI (Can't be fixed) 
- Trackpad Buttons not working properly works only when you touch trackpad touch area. (No fix for that yet)
- Some fn keys are not working its under progress.
- Numberpad is not working (Probably it never will)
- You tell me.

# Installation:
## OPENCORE
- First read opencore installation docs for more info (https://github.com/acidanthera/OpenCorePkg).
- Select best configuration for your system and use that config file into EFI/OC folder 
Example: EFI/OC/config.plist
- Edit your device SMBIOS info as MacbookPro 15.1 with your own values.(You might want to use OpenCore Configurator).
- If you want to install it only single drive install OS X first then Windows after all installation complete.
- Copy efi folder to your drive and replace boot folder. Move windows folder into OC folder. Then use bless override
section and set windows boot file location. Disable hideself in misc.
- If you have two seperate drives install with oses in any order.Copy Efi folder into OSX drive. And enable hideself in misc.
- If trackpad or sound is not working rebuild cache with  sudo kextcache -i / command.

### Installing Linux on OPENCORE
- On Opencore boot press space and open OpenCore Shell
- Find your EFI drive among these drives in the list and take a picture of its information.
- Enable Linux in Misc Entries. You can rename it.
- You need to edit path as your EFI drive it is a long text but you need to type it correctly. There are two examples in build one for M2 sata drive one for Sata SSD. If you write it correctly then opencore has to boot linux.


## Q.A:
- Q-) My bios left on black screen what can I do? 
- A-) It's common bug after catalina. Solution: Disable fast bios and use opencore for booting. 
Easy fix: Just select reset NVRAM option in opencore.

- Q-) My speaker is not working what can I do? 
- A-) Please don't forget to disable boot logo sound otherwise your speaker won't work.

- Q-) I am getting kernel panic it says ionvme error what can I do?
- A-) Your nvme ssd is most likely not supported by apple you need to replace it or buy a sata ssd and enable SSDT_NVMe-Pcc.aml in config.plist

- Q-) My keyboard backlight can't be controlled with any app what can I do?
- A-) Enable ALS0.aml from config.plist/ACPI section.

- Q-) I have bug kp error what can I do? 
- A-) Attach a debug and detailed information about bug. Without information I can't fix
anything.


