# Hardware specifications

| Component | Recorded value |
| --- | --- |
| Family | Lenovo G50, machine type 80E3 |
| Processor | AMD A8-6410 APU |
| GPU | Integrated Radeon R5 |
| Memory | 8 GB |
| SSD | Lexar NS100 256 GB |
| Ethernet | Realtek PCIe GBE Family Controller |
| Wireless | Broadcom 802.11n Network Adapter (Windows label; exact PCI ID pending) |
| Firmware boot | UEFI |
| SVM | Manually enabled in firmware |

## Notes

This laptop is intended for light browsing, typing and occasional coding; its SSD and RAM were previously upgraded. No further RAM upgrade is planned.

## To verify from Linux live session

```bash
lspci -nnk | grep -iA3 -E 'network|wireless'
rfkill list all
inxi -N
```

Record the Wi-Fi device's vendor/device ID and driver in the troubleshooting document, but redact unique machine identifiers.
