# OpenCore EFI AsRock H410M-ITX/AC i3-10100

 Stable and concise OpenCore EFI files for AsRock H410M-ITX/AC and i3-10100.



## Details of the PC Used in Debugging

| Items       | Model               |
| ----------- | ------------------- |
| Motherboard | AsRock H410M-ITX/AC |
| CPU         | Intel Core i3-10100 |
| RAM         | Kingback 8G 2400 MHz |
| Hard Disk   | Kingback 260G SSD   |
| GPU         | AMD Radeon RX560 4G |
| Sound Card  | Realtek ALC887      |
| Ethernet    | (Onboard)           |
| WLAN        | Intel Dual Band Wireless-AC 3168 |
| Monitor     | AOC 27-inch FHD     |

## Problems still exist
- ~~Meet `AppleUSBXHCIPort::resetAndCreateDevice: failed to start device` during booting with `-v`~~
> Put `USBPorts.kext` and `XHCI-unsupported.kext` into `/EFI/OC/kexts` and write these to kexts into `config.plist`.
- ~~Sound Card failed to drive~~
> AppleALC.kext with layout-id 12 is OK.
- WLAN failed to drive
- Bluetooth connection is not stable
- Can't turn off the power if you shutdown in macOS

## Author
ThrRip  
Website (Chinese only): [ThrRip's Personal Homepage](https://thrrip.space)
