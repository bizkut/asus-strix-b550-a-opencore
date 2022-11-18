# AMD Ryzen Hackintosh - Opencore EFI for ASUS ROG STRIX B550-A GAMING

## Specification
| **Component** | **Model** |
| ------------- | --------- |
| CPU | AMD Ryzen 7 5800X3D @ 3.6GHz |
| Motherboard | ASUS ROG STRIX B550-A GAMING |
| RAM | 16GB (2 x 8GB) G.SKILL Trident Z Neo DDR4-3600 CL16 |
| GPU | TUF GAMING Radeon™ RX 6800 OC Edition |
| Ethernet | Intel® I225-V 2.5Gb |
| OS Disk (NVME) | WD_BLACK SN850 NVMe™ SSD 1TB |

**macOS version**: 13.0.1

**OpenCore version**: 0.8.6

**SMBIOS**:  MacPro7,1

## Working
- Everything !
- Fixed Ethernet (Intel® I225-V 2.5Gb) issue on MacOS Ventura

## Not working
 - None (No Wifi, No trouble)

## Known Issues
 - Sleep - Wakes from sleep instantly (Maybe cause of USB Mapping?)

## BIOS Settings
 - You can use the default settings or whatever suits you but the important part is below since we enabled ReBAR in OpenCore config.
   Advanced
   -> PCI Subsystem Settings
      -> Above 4G Decoding  - Enabled
      -> Resize BAR Support - Auto

## How to use
  1. Create directory "EFI" in your EFI partition (e.g. pendrive or hard drive)
  2. Clone this repo and paste directiories "BOOT" and "OC" onto created directory
  3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as model select **MacPro7,1**.
  4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values.
  5. Boot it!  

## Credits

 * [musfiqus](https://github.com/musfiqus/hackintosh-ROG-STRIX-B550A)
 * [huukhai](https://github.com/huukhai/hackintosh-rog-b550i)
 * [ikechan8370](https://github.com/ikechan8370/Asus-B550A-Opencore-EFI.git)
 * [RadeonSensor - Kext and Gadget to show Radeon GPU temperature on macOS](https://github.com/aluveitie/RadeonSensor)
 * [AMD Vanilla OpenCore](https://github.com/AMD-OSX/AMD_Vanilla)

## Disclaimer

This documentation is published for the sole purpose of learning and tech enthusiasm and with no guarantees of any kind, I’m not responsible of any harm of any kind or loss of data that may occur.
