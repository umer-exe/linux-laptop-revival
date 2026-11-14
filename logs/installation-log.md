# Installation log 

**Machine:** Lenovo G50-45 (80E3); AMD A8-6410, Radeon R5, 8 GB RAM, Lexar NS100 256 GB SSD.

## Completed
- Enabled SVM and confirmed UEFI boot mode.
- Created a Mint 22.3 Xfce USB using Rufus on a separate desktop PC.
- First installation crashed after partitioning; intermittent laptop USB connection and I/O error observed.
- Retried from a fresh live boot and installed successfully to SSD.
- Verified sound, keyboard, display, brightness, touchpad; tap-to-click works on installed system.
- Installed Broadcom STA DKMS offline for BCM43142 (`14e4:4365`); Wi-Fi works after reboot.
- Created initial and post-update Timeshift system snapshots.
- Installed pending updates (~208 packages); verified kernel `7.0.0-43-generic` and `broadcom-sta` DKMS build.
- Installed multimedia codecs, configured Firefox Sync/extensions, trimmed autostart apps, and enabled GUFW firewall.
- Reviewed Power Manager settings and verified suspend/resume with Wi-Fi reconnection.
- Installed Broadcom Bluetooth firmware (`BCM43142A0-105b-e065.hcd`) to `/lib/firmware/brcm/`, reloaded `btusb`, and verified earbud pairing and audio.

## Paused / next
- Install and configure Git and VS Code.
- Consider LibreOffice and optional Docker Engine later.
