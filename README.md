# hackintosh
Hackintosh config

Motherboard: ASUS Prime Z390-A  
GPU: SAPPHIRE Pulse Radeon RX 5700 XT 8G GDDR6 HDMI / Triple DP OC W / BP (Uefi)  
CPU: Intel Core processor CPU 4,60 GHz  
RAM: Gskill F4-3200C16D-32GVK Memory D4 3200 32GB C16 RipV K2 2x 16GB, 1,35V  
SSD: Sabrent 1TB Rocket NVMe PCIe M.2 2280 Internal SSD High Performance Solid State Drive (SB-ROCKET-1TB)  
Case: Nzxt H510  
Power supply: Corsair RM750x  
CPU cooler: Noctua NH-U12S  
Bluetooth: Fenvi t919  

# Tricky parts:
1. CPU graphics doesn't work because of the cable I use. I use HDMI cable and could get it working with external GPU `config.plist` toggle only  
2. I had to remap some USB ports to enable Fenvi card to operate properly. I've used Hackintool for this  
3. I had to disable "F1 warning" screen in BIOS because otherwise I had to re-enter BIOS every time after MacOS reboots  

# Updating

1. Follow the official [OpenCore guide](https://dortania.github.io/OpenCore-Post-Install/universal/update.html)
2. Download the latest [OpenCore release](https://github.com/acidanthera/OpenCorePkg/releases) and update all the `.efi` and `.kext` files from the [build repo](https://dortania.github.io/builds/)
3. Use [OCConfigCompare](https://github.com/corpnewt/OCConfigCompare) to compare and update the `.plist` to the latest version
4. Use [ProperTree](https://github.com/corpnewt/ProperTree) to update the `.plist` snapshot
5. Boot from USB using freshly created EFI, copy to boot EFI partition if everything works
