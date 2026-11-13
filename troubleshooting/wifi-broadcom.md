# Broadcom Wi-Fi troubleshooting

**Status:** Wi-Fi networks don't appear in the Mint 22.3 Xfce live session. Fix not yet tested.

**Adapter:** Broadcom BCM43142, PCI ID `14e4:4365` (rev 01); Lenovo subsystem `17aa:0621`. IDs transcribed manually.

**Likely driver:** Broadcom STA (`wl` / `bcmwl-kernel-source`). May require temporary Ethernet or phone USB tethering.

## Next steps

1. Check for a blocked wireless radio: `rfkill list all`
2. Connect Ethernet or USB tethering if possible.
3. Open **Menu → Administration → Driver Manager** and check whether a Broadcom driver is offered.
4. Test Wi-Fi after installing the recommended driver; record the outcome here.

Note: Driver changes made in a non-persistent live session won't normally survive reboot or carry over to the installed system.
