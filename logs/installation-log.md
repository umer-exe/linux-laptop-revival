# Installation log — November 13, 2026

**Machine:** Lenovo G50-45 (80E3); AMD A8-6410, Radeon R5, 8 GB RAM, Lexar NS100 256 GB SSD.

## Completed
- Enabled SVM and confirmed UEFI boot mode.

- Created a Mint 22.3 Xfce USB using Rufus on a separate desktop PC.

- First installation crashed after partitioning; intermittent laptop USB connection and I/O error observed.

- Retried from a fresh live boot and installed successfully to SSD.

- Verified sound, keyboard, display, brightness, touchpad; tap-to-click works on installed system.

- Installed Broadcom STA DKMS offline for BCM43142 (`14e4:4365`); Wi-Fi works after reboot.

- Created the first Timeshift system snapshot.

- Installed pending system updates and verified kernel `7.0.0-43-generic` (`linux-image-7.0.0-43-generic`) with `broadcom-sta/6.30.223.271` built via DKMS.

- Configured Firefox Sync, extensions, autostart apps, and GUFW firewall.

- Reviewed Xfce Power Manager settings and verified suspend/resume with automatic Wi-Fi reconnection.


## Paused / next
- Install and configure Git and VS Code.

- Consider LibreOffice and optional Docker Engine later based on workload needs.
