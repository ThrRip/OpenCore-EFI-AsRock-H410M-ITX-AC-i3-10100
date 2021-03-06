# OpenCore EFI AsRock H410M-ITX/AC i3-10100

 Stable and concise OpenCore EFI files for AsRock H410M-ITX/AC and i3-10100.



## Details of the PC Used in Debugging

| Items       | Model               |
| ----------- | ------------------- |
| Motherboard | AsRock H410M-ITX/AC |
| CPU         | Intel Core i3-10100 |
| RAM         | Team 8G 2400 MHz    |
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
- ~~WLAN failed to drive~~
  > Now we can use Airportitlwm.kext to make almost every Intel WLAN Card work. See [here](https://openintelwireless.github.io/itlwm/Installation.html#airportitlwm) for more information.
- ~~Bluetooth connection is not stable~~
  > Resolved after adding `IntelBluetoothFirmware.kext` and `IntelBluetoothInjector.kext`.
- Can't turn off the power if you shutdown in macOS

## Author
ThrRip  
Website (Chinese only): [ThrRip's Personal Homepage](https://thrrip.space)

## Reminder
Because I don't have much time, this project has been archived on January 7, 2021 (UTC+8), and will not be maintained after that.
