# Broadcom Wi-Fi not detected / no networks appear

**Status: investigating. No fix confirmed.**

## Symptoms
On the Linux Mint 22.3 Xfce live USB session, nearby Wi-Fi networks do not appear.

Windows reported a **Broadcom 802.11n Network Adapter**, but this generic name does not establish the Linux driver required.

## Diagnose

Open a terminal in the live session:

```bash
lspci -nnk | grep -iA3 -E 'network|wireless'
rfkill list all
inxi -N
```

Note the PCI vendor/device ID (for example `[14e4:xxxx]`), the `Kernel driver in use` line (if any), and any soft/hard block from `rfkill`.

If the device is soft-blocked, check the network toggle / airplane mode first. If it is hard-blocked, check the laptop's wireless switch or Fn key.

## Important

Do **not** assume that every Broadcom adapter needs the proprietary `bcmwl-kernel-source` / `wl` driver. Driver choice depends on the PCI ID and kernel support. The live USB may require Ethernet or USB tethering to install driver packages.

## Resolution
_Not yet determined. Update after the exact chipset and driver are identified._
