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

## Paused / next
- Installed the previously pending updates. After reboot, Wi-Fi reconnects and Firefox, touchpad and sound work.
- Kernel reported as `7.0.0-43-generic` (verify exact output and package source; unusual for this Mint release).
- After updates, verify Wi-Fi still works, particularly if the kernel changes.
- Finish browser, writing apps, Git, VS Code, Codex and optional Docker setup.
- Test suspend/resume and measure day-to-day responsiveness.
