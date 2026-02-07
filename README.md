# Custom BIOS Mods for various platforms
- This repository contains only the modded BIOS files.
- No instructions are given. USE AT YOUR OWN RISK IF YOU KNOW WHAT YOU ARE DOING. NO SUPPORT OR GUARANTEE IT WILL WORK FOR YOU!

# Important Notes:
- BACKUP YOUR BIOS BEFORE FLASHING!!
- FLASH ANY BIOS ON YOUR OWN RISK ONLY !!

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

# HUANANZHI X10X99 16D
- Custom BIOS for HUANANZHI X10X99-16D motherboard
- Various BIOS mods with S3 Turbo Unlock and -0mv to -100mv undervolting.
- Best flashed using CH341A (green 3.3V) + SOIC8 Clip directly to the W25Q128JV chip. First power on may take a while and reboot often. Reset BIOS to defaults and reconfigure on first boot. 

```
X10X9916DV13-0.bin
X10X9916DV13-50.bin
X10X9916DV13-60.bin
X10X9916DV13-70.bin
X10X9916DV13-80.bin
X10X9916DV13-90.bin
X10X9916DV13-100.bin
```
- Original vendor BIOS v1.3 ```9916DV13.bin``` as from source:```X10X99-16D V1.3 23-10-24 优化解决不能通过U盘升级BIOS问题.rar```

- Note: This motherboard does need updated BMC for better fan control. Make sure you have updated the BMC SOC flash as well.
  Check with vendor on updated released directly! Use below links at your own risk!

- If system freezes randomly when using the modified BIOS try these steps at your own risk:
    - Use following kernel parameters at your own risk ```pcie_aspm=off intel_pstate=disable intel_idle.max_cstate=1``` if you run Linux
    - Cool your VRM. 
    - Undervolt more (eg from -50 to -60 or -70) or less.. (only if you know why)
    - Revert back to stock BIOS if you can not fix it.

- Vendor Links:
  [Official BMC firmware](https://drive.google.com/file/d/13n3X6cydaHWNnvgJijHUf6cQ-x7x8e5b/edit)
  [Official BIOS X10X99-16D V1.3 23-10-24](https://drive.google.com/file/d/1R2hj4ygJ9yF1kbl6d4wDdewC35Riamzc/edit)
