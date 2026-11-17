# Hardware specifications

| Component | Recorded value |
| --- | --- |
| Laptop | Lenovo G50-45 (machine type 80E3) |
| Processor | AMD A8-6410 APU |
| Graphics | Integrated Radeon R5 |
| Memory | 8 GB; no further upgrade planned |
| Primary Storage | Lexar NS100 256 GB SSD (`/` root) |
| Secondary Storage | Seagate 500 GB HDD (`ST500LT012-1DG142`) via 9.5mm optical bay SATA caddy (`/mnt/hdd`) |
| Display | 15.6" TN (`1366x768`, output `eDP`) |
| Ethernet | Realtek PCIe GBE Family Controller (`10ec:8168`) |
| Wireless | Broadcom BCM43142 (`14e4:4365`), Lenovo subsystem `17aa:0621` |
| Boot mode | UEFI |
| SVM | Enabled |
| OS | Linux Mint 22.3 Xfce |
| Kernel at Wi-Fi fix | `6.14.0-37-generic` |

Intended use: browsing, typing and lightweight development. The Broadcom STA driver was installed offline and remains functional after reboot.

## Secondary storage mount

The 500 GB optical bay HDD is formatted as a single `ext4` partition (`UUID=fc1ae531-50e5-405c-9d83-87c974f240d3`) and configured via GNOME Disks (`/etc/fstab`) to auto-mount at `/mnt/hdd` with `nofail` enabled.

## Display calibration

To compensate for the TN panel's cool tint and washed-out contrast, gamma and RGB balance are adjusted via `xrandr`:

```bash
xrandr --output eDP --gamma 0.80:0.80:0.75
```

To revert to default display values:

```bash
xrandr --output eDP --gamma 1.0:1.0:1.0
```

Persisted across reboots via Xfce **Session and Startup → Application Autostart** (`on login`).
