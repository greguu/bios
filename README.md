# Custom BIOS Mods for various platforms
- This repository contains only the modded BIOS files.
- No instructions are given. USE AT YOUR OWN RISK IF YOU KNOW WHAT YOU ARE DOING. NO SUPPORT OR GUARANTEE IT WILL WORK FOR YOU!

# Checkpoint 4800 / T-180
- This custom BIOS does add Intel XEON support for the CheckPoint 4800 Firewall.
- Some XEON CPUs are more energy efficient, compared to the stock Core 2 Quad Q9400 with 95W TDP.
- This was tested successfully with a XEON L5408 CPU, although it may work with other CPU from this family*.
- *Added BIOS support for cpu10676_plat40_ver00000612_2015-08-02_PRD_B6F50E9C

Confirmed working:
- XEON L5408
- Processor Base Frequency 2.13 GHz
- Cache 12 MB L2 Cache
- Bus Speed 1066 MHz
- FSB Parity No
- TDP 40 W

Notes: 
- Not only the BIOS, but the CPU also needs to be modded for this to work! Check about how 771 Xeons can run in 775 boards !!
- You need to flash the BIOS using a CH471a programmer, luckily the BIOS chip is removable and its easy to do.

Important Notes:
- BACKUP YOUR BIOS BEFORE FLASHING!!
- FLASH THIS BIOS ON YOUR OWN RISK ONLY !!


# HUANANZHI X10X99 16D
- Custom BIOS for HUANANZHI X10X99-16D motherboard -> 9916DV13.bin
- This custom BIOS adds S3 Turbo Unlock and -60mv undervolting.
- Tested fine and stable with dual XEON E5-2698v3 CPUs.
- This commit also includes the original vendor BIOS v1.3 -> 9916DV13_org.bin
- May add other variants of this BIOS on demand.

Note: This motherboard does need updated BMC for better fan control. Make sure you have updated the BMC SOC flash as well.
